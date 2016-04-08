---
title: [POST] Create an article by specify GUID
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a1f834de-9dac-4e4e-b601-8f8d6a8ddfd6
---
# [POST] Create an article by specify GUID
**Description:** Create an article by specify GUID  

**API type:** POST

**URI:** v1/Projects/{projectid}/Articles
  

**Parameters:**  

	ProjectId
	  
	Request body:  
	[
        {
        "locales": [
            {
                "locale": "en-US",
                "parent_id": "parentIdToAdd",
                "default_locale": "en-US",
                "metadata": {
                    "content_class": "DDUE.Conceptual",
                    "name": "nameToAdd"
                },
                "blobs": [
                    {
                        "blob_id": "blobIdToAdd",
                        "blob_type": "Source",
                        "filename": "123.xml",
                        "filesize": 9000
                    }
                ]
            }
        ],
        "entity_id": "IDToAdd",
        "entity_type": "Article"
        }
    ]
 

**Note:**   

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Articles
	  
	Body:
	[
    {
        "locales": [
            {
                "locale": "en-US",
                "parent_id": "6c294e7c-1c1b-4562-bd08-b7ca24e2a957",
                "default_locale": "en-US",
                "metadata": {
                    "content_class": "DDUE.Conceptual",
                    "name": "TitleExample1"
                },
                "blobs": [
                    {
                        "blob_id": "f2ec1166-a87a-4623-810d-84e1e6d14d22",
                        "blob_type": "Source",
                        "filename": "123.xml",
                        "filesize": 9000
                    }
                ]
            }
        ],
        "entity_id": "6c294e7c-1c1b-4562-bd08-b7ca24e2a950",
        "entity_type": "Article"
    }
    ]


**Sample Response 1:** 

	[
        {
            "entity_id": "6c294e7c-1c1b-4562-bd08-b7ca24e2a951",
            "error_code": 0
        }
    ]


**Code Example:** 
```
        public Boolean CreateTopic(String topicName, String topicBody, Guid entityGuid,String docSetName, Boolean topicExist, String blobId)
        {
            Boolean success = false;
            try
            {
              //create the entity by GUID
              string apiurl = String.Format("https://caps-api-{0}.azurewebsites.net", _tenentName);
              string topicUrl = String.Format("/v1/Projects/{0}/Articles", repo.repoInfo.entity_id);
              string apiUrlAction = String.Format("{0}{1}", apiurl, topicUrl);
              string postData = common.POSTENTITYDATA("RequestBodyExample.txt", bodyUploadResp.blob_id, topicName, dse.entity_id, entityGuid.ToString());
              string json = common.POST(apiUrlAction, postData, "application/json;charset=utf-8");
              List<Entity_Create_Response> entityCreateResp = new List<Entity_Create_Response>();
              entityCreateResp = JsonConvert.DeserializeObject<List<Entity_Create_Response>>(json);
            }
            catch (Exception ex)
            {
                // TODO: Log exception
                return false;
            }
        }
		
         public string POSTENTITYDATA(string topicTemplete, string blobId, string topicName,string parentId, string guid)
         {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(topicTemplete))
                {
                    postData = sr.ReadToEnd();
                    postData = postData.Replace("blobIdToAdd", blobId);
                    postData = postData.Replace("nameToAdd", topicName);
                    postData = postData.Replace("parentIdToAdd", parentId);
                    postData = postData.Replace("IDToAdd", guid);
                }

                return postData;
            }
            catch (Exception ex)
            {
                // TODO: Log exception
                return postData;
            }
         }
        
		public static string POST(string url, string body, string contentType)
        {
            return Request(url, body, contentType, "POST");
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

        
        public class Entity_Create_Response
        {
            [JsonProperty(PropertyName = "entity_id")]
            public string entity_id { get; set; }
            [JsonProperty(PropertyName = "locale")]
            public string locale { get; set; }
            [JsonProperty(PropertyName = "is_success")]
            public string is_success { get; set; }
            [JsonProperty(PropertyName = "error_message")]
            public string error_message { get; set; }
        }
```