---
title: [PUT] Checkout Article
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b8f0d77-6b4e-4b61-8c39-0169f46c6d22
---
# [PUT] Checkout Article
**Description:** Checkout an article  

**API type:** PUT

**URI:** v1/Projects/{projectid}/Articles/CheckOut?locale={locale}

**Parameters:**  

	ProjectId  
	Locale  
	  
	Request body:  
	[  
	  {  
	    "id": "IDToAdd",  
	    "locales": [  
	      {  
	        "locale": "en-US",  
	        "blobs": [  
	          {  
	            "id": "blobIdToAdd",  
	            "type": "Source",  
	            "entity_id": "blobIdToAdd",  
	            "blob_id": "blobIdToAdd",  
	            "entity_type": "Source",  
	            "blob_type": "Source"  
	          }  
	        ]  
	      }  
	    ],  
	    "entity_id": "IDToAdd",  
	    "blob_id": "IDToAdd"  
	  }  
	]  
	  
**Note:** Make sure the articles did not checkout by other people  

**Sample Request 1:** 

	PUT https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Articles/CheckOut?locale=en-US  
	  
	[  
	  {  
	    "id": "example-60822377-da7a-40b8-0089-d185d1509344",  
	    "locales": [  
	      {  
	        "locale": "en-US",  
	        "blobs": [  
	          {  
	            "id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",  
	            "type": "Source",  
	            "entity_id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",  
	            "blob_id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",  
	            "entity_type": "Source",  
	            "blob_type": "Source"  
	          }  
	        ]  
	      }  
	    ],  
	    "entity_id": "example-60822377-da7a-40b8-0089-d185d1509344",  
	    "blob_id": "example-60822377-da7a-40b8-0089-d185d1509344"  
	  }  
	]  
	  
**Sample Response 1:** 

	[  
	  {  
	    "locales": [  
	      {  
	        "children_url": "https://caps-api-devint.azurewebsites.net/v1/projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/articles/5714a225-befd-438a-9bb5-f6fdc50a4ef1:(children)",  
            "locale": "en-US",  
	        "blobs": [  
	          {  
	            "blob_id": "5714a225-befd-438a-9bb5-f6fdc50a4ef1-521898563",  
	            "created_at": "2015-08-12T09:54:10Z",  
	            "created_by": "4422b87327c34d3b84941e0fd91a5a2a",  
	            "updated_at": "2015-08-12T09:54:10Z",  
	            "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",  
	            "revision": 1,  
	            "blob_type": "BuildInternal",  
	            "filesize": 0,  
	            "word_count": 0,  
	            "content_url": "https://caps-api-devint.azurewebsites.net/v1/projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/articles/5714a225-befd-438a-9bb5-f6fdc50a4ef1:(blobcontent(BuildInternal))?locale=en-US"  
	          },  
	          {  
	            "blob_id": "ddb686e5-249e-4372-8af6-d3f5a4f3675c",  
	            "checkout_by": "afb4736e-f853-49db-b42c-db391da18e9e",  
	            "checkout_at": "2015-08-12T09:54:21Z",  
	            "created_at": "2015-08-12T09:54:09Z",  
	            "created_by": "a658d6b6-26d4-465c-bcbc-904800534202",  
	            "updated_at": "2015-08-12T09:54:09Z",  
	            "updated_by": "a658d6b6-26d4-465c-bcbc-904800534202",  
	            "revision": 1,  
	            "blob_type": "Source",  
	            "filesize": 0,  
	            "word_count": 0,  
	            "content_url": "https://caps-api-devint.azurewebsites.net/v1/projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/articles/5714a225-befd-438a-9bb5-f6fdc50a4ef1:(blobcontent(Source))?locale=en-US"  
	          }  
	        ],  
	        "metadata_url": "https://caps-api-devint.azurewebsites.net/v1/projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/articles/5714a225-befd-438a-9bb5-f6fdc50a4ef1:(metadata)?locale=en-US",  
	        "blobs_url": "https://caps-api-devint.azurewebsites.net/v1/projects/811c88a0-c18f-497d-b20b-2185cc2bb79c/articles/5714a225-befd-438a-9bb5-f6fdc50a4ef1:(blob)?locale=en-US",  
	        "metadata": {  
	          "is_deleted": false,  
	          "is_mtps_no_follow": false,  
	          "is_mtps_no_index": false,  
	          "is_not_in_toc": false,  
	          "is_pave_over": false,  
	          "is_root": false,  
	          "name": "Add Columns",  
	          "preview_buildjob_id": "5714a225-befd-438a-9bb5-f6fdc50a4ef1--preview",  
	          "publish_source_version": "1.0",  
	          "ready_for_localizaion": true,  
	          "ready_to_promote": false,  
	          "ready_to_stage": false,  
	          "source_version": "1.0",  
	          "status": "writing not started",  
	          "entity_type": "Article",  
	          "entity_id": "5714a225-befd-438a-9bb5-f6fdc50a4ef1",  
	          "locale": "en-US",  
	          "created_by": "a658d6b6-26d4-465c-bcbc-904800534202",  
	          "created_at": "2015-08-12T09:54:09Z",  
	          "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",  
	          "updated_at": "2015-08-12T09:54:11Z",  
	          "revision": 4,  
	          "has_container": false  
	        }  
	      }  
	   ],  
	   "entity_id": "5714a225-befd-438a-9bb5-f6fdc50a4ef1",  
	   "entity_type": "Article"  
	  }  
	]  
	
**Code Example:**
```
      public Boolean CheckOutArticle(String entityId,String blobId)
      {
            try
            {
                String apiurl = String.Format("https://caps-api-{0}.azurewebsites.net" _tenentName);
                String topicUrl = String.Format("/v1/Projects/{0}/Articles/CheckOut?locale=en-US", _pro);
                String apiUrlAction = String.Format("{0}{1}", apiurl, topicUrl);

                String postData = common.PUTCHECKOUTDATA("RequestBodyExample.txt", entityId, blobId);
                string json = common.PUT(apiUrlAction, postData,  "application/json;charset=utf-8");

                return true;
            }
            catch
            {
                // TODO: Log exception
                return false;
            }
        }
		
		public string PUTCHECKOUTDATA(string topicTemplete, string entityId, string blobId)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(topicTemplete))
                {
                    postData = sr.ReadToEnd();
                    postData = postData.Replace("IDToAdd", entityId);
                    postData = postData.Replace("blobIdToAdd", blobId);
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
