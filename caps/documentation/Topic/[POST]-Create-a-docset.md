---
title: [POST] Create a docset
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ee4d052-d109-40ce-99be-a9482de538ed
---
# [POST] Create a docset
**Description:** Create a docset  

**API type:** POST

**URI:** v1/Projects/{ProjectId}/Containers?type=docset  
  

**Parameters:**  

	ProjectId  
	
	Request Body
	[  
	 {  
	  "metadata":  
	      {  
	       "class":"DocSet",  
	           "name":"nameToAdd"  
	      },  
	           "parent_id":"parentIdToAdd",  
	           "entity_type":"Container"  
	 }  
	]  

	  
**Note:** N/A

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Containers?type=docset  
	  
	Body:  
	[  
	 {  
	  "metadata":  
	      {  
	       "class":"DocSet",  
	           "name":"Example"  
	      },  
	           "parent_id":"e0bbf1ff-22a9-4533-93de-823e91a3d49b",  
	           "entity_type":"Container"  
	 }  
	]  
	  

**Sample Response 1:** 

	[  
	 {  
	  "entity_id": "d921f79b-16f4-45ec-8c2f-d725e1d7d33a",  
	  "error_code": 0  
	 }  
	]  
	
**Code Example:** 

```
        public Boolean CreateDocSet(String name)
        {
            String docsetTocId = String.Empty;
            String docsetEntityId = String.Empty;
            try
            {
                String apiurl = String.Format("https://caps-api-{0}.azurewebsites.net", _tenentName);
                String createDocSetUrl = string.Format("{0}{1}", apiurl, String.Format("/v1/Projects/{0}/Containers?type=docset", repo.repoInfo.repository_id));
                String postData = POSTDOCSETDATA("RequestBodyExample.txt", name, repo.docSetsEntityID);
                string json = POST(createDocSetUrl, postData, "application/json;charset=utf-8");
                List<DocSet_Create_Response> dcrList = JsonConvert.DeserializeObject<List<DocSet_Create_Response>>(json);
                }
                return true;
            }
            catch (Exception ex)
            {
                 // TODO: Log exception
                return false;
            }
        }
        
        public string POSTDOCSETDATA(string docsetTemplete, string name, string parentId)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(docsetTemplete))
                {
                    postData = sr.ReadToEnd();
                    postData = postData.Replace("nameToAdd", name);
                    postData = postData.Replace("parentIdToAdd", parentId);
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

        public class DocSet_Create_Response
        {
            [JsonProperty(PropertyName = "entity_id")]
            public string entity_id { get; set; }
            [JsonProperty(PropertyName = "error_code")]
            public int error_code { get; set; }
        }
```

	 