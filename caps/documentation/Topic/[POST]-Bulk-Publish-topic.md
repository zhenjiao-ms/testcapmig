---
title: [POST] Bulk Publish topic
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2bb74af-a8ec-4de7-be35-960146ab1988
---
# [POST] Bulk Publish topic
**Description:** Bulk Publish topic  

**API type:** POST

**URI:**  v2/Projects/{projectID}/EntityJob/Article
  

**Parameters:**  

	ProjectId
	  
	Request body:  
    {
    "locale": "en-US",
    "job_type": "BatchUpdate",
    "include_entity_ids": [
        "c034e233-668b-47a7-a0e4-47dfc3e732cd",
        "c121f054-21f5-45de-a454-86e044dd1d16"
    ],
    "mode": "Auto",
    "extra": {
        "changes": {
            "ready_to_stage": true,
            "ready_to_promote": true,
            "ms_topic": "get-started-article"
        },
        "delta_changes": {}
    },
    "fields": [
        "ready_to_stage",
        "ready_to_promote",
        "ms_topic"
    ]
    }

    
 

**Note:**   ProjectID is required

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v2/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/EntityJob/Article 
	  
	Body:
     {
    "locale": "en-US",
    "job_type": "BatchUpdate",
    "include_entity_ids": [
        "c034e233-668b-47a7-a0e4-47dfc3e732cd",
        "c121f054-21f5-45de-a454-86e044dd1d16"
    ],
    "mode": "Auto",
    "extra": {
        "changes": {
            "ready_to_stage": true,
            "ready_to_promote": true,
            "ms_topic": "get-started-article"
        },
        "delta_changes": {}
    },
    "fields": [
        "ready_to_stage",
        "ready_to_promote",
        "ms_topic"
    ]
    }



**Sample Response 1:** 

  	[
       {
         "job_type": "BuildJob",
         "run_id": "8587562882245878101",
         "entity_id": "da180f8a-6d2e-4c09-88e5-da8372be2936---publish",
         "locale": "en-US",
         "error_code": 0
     }
    ]



**Code Example:** 
```
     public bool PublishToStaging(string projectId)
    {
        try
        {
            string publishUrl = string.Format("v2/Projects/{projectID}/EntityJob/Article", projectId);
            string apiUrlAction =string.format("{0}{1}","https://caps-api-{0}.azurewebsites.net" ,publishUrl);
            string postData = _common.POSTTOPICDATA("RequestBodyExample.txt");
           string json=POST(apiUrlAction,postData,"application/json;charset=utf-8");
            return true;
        }
        catch (Exception ex)
        {
            // TODO: Log exception
            return false;
        }
    }
public string POSTTOPICDATA(string _topicTemplete)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(_topicTemplete))
                {
                    postData = sr.ReadToEnd();
                }
                return postData;
            }
            catch (Exception ex)
            {
                return postData;
            }
        }
public static string POST(string url, string body, string contentType)
    {
        return Request(url, body, contentType, "POST");
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