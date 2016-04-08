---
title: [PUT] Update CAPS Metadata (Toc General and Publish)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dc4e133-12ec-44af-aa8f-7c16ce55d81d
---
# [PUT] Update CAPS Metadata (Toc General and Publish)
**Description:** Update CAPS Metadata (Toc General and Publish)  

**API type:** PUT

**URI:** v1/Projects/{ProjectId}/Articles?locale=en-US 

**Parameters:**  

	ProjectId  
	  
	Toc - Request body:  
	[  
	  {  
	    "id": "idToAdd",  
	    "type": "Article",  
	    "locales": [  
	      {  
	        "locale": "en-US",  
	        "metadata": {  
	          "metadataToAdd"  
	       }  
	     }  
	   ],  
	   "entity_id": "idToAdd",  
	   "blob_id": "idToAdd",  
	   "entity_type": "Article",  
	   "blob_type": "Article"  
	  }  
	]  
	  
**Note:** Make sure the attribute is accurate  

**Sample Request 1:** 

	PUT https://caps-api-devint.azurewebsites.net/v1/Projects/05f57908-75ce-4769-bd3d-1528c9cba379/Articles?locale=en-US 
	  
	[  
	  {  
	    "id": "15dc5298-8dc3-4d77-ab4f-ab5036a57747",  
	    "type": "Article",  
	    "locales": [  
	      {  
	        "locale": "en-US",  
	        "metadata": {  
	          "ready_to_stage": false,  
	          "ready_to_promote": false,  
	          "ms_devlang": [  
	            "dotnet",  
	            "javascript",  
	            "php"  
	          ],  
	          "ms_topic": "index-page ",  
	          "is_mtps_no_index": false,  
	          "is_mtps_no_follow": false,  
	          "community_content": false  
	        }  
	      }  
	    ],  
	    "entity_id": "15dc5298-8dc3-4d77-ab4f-ab5036a57747",  
	    "blob_id": "15dc5298-8dc3-4d77-ab4f-ab5036a57747",  
	    "entity_type": "Article",  
	    "blob_type": "Article"  
	  }  
	]  

	  
**Sample Response 1:** 

	[  
	  {  
	    "entity_id": "15dc5298-8dc3-4d77-ab4f-ab5036a57747",  
	    "error_code: 0  
	  }  
	]
	
**Code Example:**
```
        public string UpdateMetadata(string url, string guid,string entityId, string proID, string type, string RepositoryID)
        {
            try
            {
                if (type == Strgeneral || type == Strpublish || type == StrDocSetpublish)
                {
                    PublishputData = common.PUTMETADATA(guid, entityId, proID, type);
                }
               // update the Meatadata, and return result

                var responseStream = common.PUT(url, RepositoryID, PublishputData, "application/json;charset=utf-8");
                return "true";
            }
            catch (Exception Ex)
            {
                // TODO: Log exception
                return Ex.ToString();
            }
        }
		
		public string PUTMETADATA(string guid,string entityId, string proID,string type)
        {
            string postData = "";
            try
            {
				using (StreamReader sr = new StreamReader("RequestBodyExample.txt"))
                {
				    postData = sr.ReadToEnd();
                    postData = postData.Replace("idToAdd", guid);
                    postData = postData.Replace("metadataToAdd", "[]");
                }
               }
                return putData;
            }
            catch (Exception ex)
            {
                // TODO: Log exception
                return putData;
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