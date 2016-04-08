---
title: [POST] Publish topic to Live
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe3c6835-23d0-452c-ba73-099dcd9bb5db
---
# [POST] Publish topic to Live
**Description:** Publish topic to Live  

**API type:** POST

**URI:**  v2/Projects/{ProjectId}/Promote?docSetId={docSetid}&locale={locale}
  

**Parameters:**  

	ProjectId
    docSerId
    locale
	  
	Request body:  
	
    {
       "outline_ids": [
      "1cd36e7b-5ba3-4aa6-92b3-5ce966b5a208"
      ],
      "publish_option": "both",
      "with_children": true,
      "force_ready": true,
      "force_rebuild": true
    }
    
 

**Note:**   

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v2/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/Promote?docSetId=da180f8a-6d2e-4c09-88e5-da8372be2936&locale=en-US
	  
	Body:
    {
       "outline_ids": [
      "1cd36e7b-5ba3-4aa6-92b3-5ce966b5a208"
      ],
      "publish_option": "both",
      "with_children": true,
      "force_ready": true,
      "force_rebuild": true
    }


**Sample Response 1:** 

  	[
       {
         "job_type": "BuildJob",
         "run_id": "8587562961622435139",
         "entity_id": "da180f8a-6d2e-4c09-88e5-da8372be2936--promote",
         "locale": "en-US",
         "error_code": 0
     }
    ]



**Code Example:** 
```
        public bool PublishToLive(string projectId, string docSetId, string locale)
    {
        try
        {
            string publishUrl = string.Format("/v2/Projects/{projectId}/Promote?docSetId={docSetId}&locale={locale} ", projectId,docSetId,locale);
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