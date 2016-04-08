---
title: [POST] Upload content
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a15fe65e-e962-4a41-897f-077af51260c0
---
# [POST] Upload content


**Http Verb** POST

## URI Template 
```
v1/Projects/{ProjectId}/TempFiles?locale=en-US&contentClass={ContentClass}
```

## Parameters 

| Parameter | Required | Description |
| --- | --- | --- |
| ProjectId | | Project id |
| ContentClass | | Blob type. One of (_$todo: what are the ContentClass values?) |

## Request Body
	
Content-Type: multipart/form-data; boundary=---------------------------7df25d1330476  
----------------------------7df25d1330476  
Content-Disposition: form-data; name="BlobData"  
[actual blob content ]  
-----------------------------7df25d1330476
	  

##Sample Request
```
POST https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/TempFiles?locale=en-US 
```
### Response
```
[  
  {  
    "blob_id": "fbcc0e78-212a-4d3b-a28c-eb14678d35d2",  
    "error_code: 0  
  }  
]  
```

## Code Example 
```
    //Upload the content of the topic
    public bool CreateTopic(string topicName, string topicBody, string templateType)
    {
        try
        {
            string topicUrl = string.Format("/v1/Projects/{0}/TempFiles?locale=en-US&contentClass={1}", _repo.Repository_id, templateType);
            string apiUrlAction = _apiUrl + topicUrl;
            topicBody = string.Format("\x0d\x0a{0}\x0d\x0a", topicBody);
            string postData = string.Concat(
                "-----------------------------7df25d1330476\x0d\x0a",
                "Content-Disposition: form-data; name=\"BlobData\"\x0d\x0a",
                topicBody,
                "\x0d\x0a-----------------------------7df25d1330476--\x0d\x0a");
            string json = _common.POST(apiUrlAction, postData, "multipart/form-data; boundary=---------------------------7df25d1330476");

            UploadResponse bodyUploadResp = JsonConvert.DeserializeObject<UploadResponse>(json);
            return true;
        }
        catch (Exception ex)
        {
            // TODO: Log exception
            return false;
        }
    }

    public static string POST(string url, string body, string contentType)
    {
        return Request(url, body, contentType, "POST");
    }

    public static void TextRequestBody(HttpWebRequest request, string body, Encoding encoding)
    {
        if (!string.IsNullOrEmpty(body))
        {
            byte[] bytes = encoding.GetBytes(body);
            request.ContentLength = bytes.Length;
            using (var stream = request.GetRequestStream())
            {
                stream.Write(bytes, 0, bytes.Length);
            }
        }
        return request;
    }

    public static string ResponseText(HttpWebRequest request, Encoding encoding)
    {
        using (HttpWebResponse response = request.GetResponse() as HttpWebResponse)
        {
            using (StreamReader sr = new StreamReader(response.GetResponseStream(), encoding))
            {
                return sr.ReadToEnd();
            }
        }
    }

    private string Request(string url, string body, string contentType, string requestType)
    {
        HttpWebRequest request = WebRequest.Create(url) as HttpWebRequest;
        request.Headers.Add(string.Format("TokenType: {0}", _tokenType));
        request.Headers.Add(string.Format("Authorization: {0}", _authorization));
        request.ContentType = contentType;
        request.Method = requestType;
        TextRequestBody(request, body, Encoding.UTF8);

        return ResponseText(request, Encoding.UTF8);
    }
```