---
title: [PUT] Checkin Article
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 66137cbd-0b03-40de-8383-73c789686e06
---
# [PUT] Checkin Article
**Description:** Checkin an article  

**API type:** PUT

**URI:** v1/Projects/{projectid}/Articles/CheckIn?locale={locale}

**Parameters:**  

	ProjectId  
	Locale  
	  
	Request body:  
	[
    {
        "entity_id": "IDToAdd",
        "entity_type": "Article",
        "locales": [
            {
                "locale": "en-US",
                "blobs": [
                   	 {
                        "comments": "Update By MLCapsImport Tool",
                        "blob_id": "blobIdToAdd",
                        "blob_type": "Source"
                    	}
                	]
            	}
        	]
    	}
	]
	  
**Note:**  

**Sample Request 1:** 

	PUT https://caps-api-devint.azurewebsites.net/v1/Projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/Articles/CheckIn?locale=en-US
	  
	[
    {
        "entity_id": "example-60822377-da7a-40b8-0089-d185d1509344",
        "entity_type": "Article",
        "locales": [
            {
                "locale": "en-US",
                "blobs": [
                    	{
                        "comments": "asd",
                        "blob_id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",
                        "blob_type": "Source"
                    	}
                	]
            	}
        	]
    	}
	]
  
	  
**Sample Response 1:** 

	[
    	{
        	"entity_id": "5714a225-befd-438a-9bb5-f6fdc50a4ef1",
        	"error_code": 0
    	}
	]
 
	
**Code Example:**
```
        public Boolean CheckOutArticle(String entityId,String blobId)
        {
            try
            {
                String apiurl = String.Format("https://caps-api-{0}.azurewebsites.net" _tenentName);
                String topicUrl = String.Format("/v1/Projects/{0}/Articles/CheckIn?locale=en-US", _pro);
                String apiUrlAction = String.Format("{0}{1}", apiurl, topicUrl);

                String json = common.PUTCHECKOUTDATA("RequestBodyExample.txt", entityId, blobId);
                var responseStream = common.PUT(apiUrlAction, postData,  "application/json;charset=utf-8");
                return true;
            }
            catch
            {
                // TODO: Log exception
                return false;
            }
        }
		
		public string PUTCHECKOUTDATA(string _topicTemplete, string _entityId, string _blobId)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(_topicTemplete))
                {
                    postData = sr.ReadToEnd();
                    postData = postData.Replace("IDToAdd", _entityId);
                    postData = postData.Replace("blobIdToAdd", _blobId);
                }

                return postData;
            }
            catch (Exception ex)
            {
                // TODO: Log exception
                return postData;
            }
        }
		
		public string PUT(string url, string postData, string contentType)
        {
            return Request(url, postData, contentType, "PUT");
        }
        
        private string Request(string url, string postData, string contentType, string requestType)
        {
            string json;
            HttpWebRequest request = WebRequest.Create(url) as HttpWebRequest;
            request.Headers.Add(String.Format("TokenType: {0}", TokenType));
            request.Headers.Add(String.Format("Authorization: {0}", Athorization));
            request.ContentType = _contentType;
            request.Method = requestType;
            Byte[] byteArray = Encoding.UTF8.GetBytes(postData);
            request.ContentLength = byteArray.Length;
            using (var Stream = request.GetRequestStream())
            {
                Stream.Write(byteArray, 0, byteArray.Length);
            }
            HttpWebResponse response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();
            using (StreamReader sr = new StreamReader(responseStream, true))
            {
                json = sr.ReadToEnd();
            }
            responseStream.Close();
            response.Close();
            return json;
        }

```