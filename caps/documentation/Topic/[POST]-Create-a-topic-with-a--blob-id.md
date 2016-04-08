---
title: [POST] Create a topic with a  blob id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 25ff3584-e5ed-43f5-91d8-bffea0747ebe
---
# [POST] Create a topic with a  blob id
**Description:** Create a project with a blob id  

**API type:** POST

**URI:** v2/Projects/{ProjectId}/Outlines  

**Parameters:**  

	ProjectId
	  
	Request body:  
	[  
	 {  
	  "entity_type": "Outline",  
	  "source_type": "Article",  
	  "parent_id": "parentIdToAdd",  
	  "locale": "en-US",  
	  "name": "nameToAdd",  
	  "state": "Normal",  
	  "content_class": "DDUE.Conceptual",  
	  "is_root": false,  
	  "writer": "writerIdToAdd",  
	  "blobs": [  
	   {  
	    "blob_id": "blobIdToAdd",  
	    "blob_type": "Source",  
	    "filename": "123.xml",  
	    "filesize": 900  
	   }  
	  ]  
	 }  
	]  

**Note:**   

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v2/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Outlines
	  
	Body:
	[
  	{
    	"entity_type": "Outline",
    	"source_type": "Article",
    	"parent_id": "6b203de9-c4de-46ab-a4ff-b9c696e75bff",
    	"locale": "en-US",
    	"name": "Test Example",
    	"state": "Normal",
    	"content_class": "DDUE.Conceptual",
    	"is_root": false,
    	"writer": "520f844609a04431b66642169a3954a7",
    	"blobs": [
      	{
        	"blob_id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",
        	"blob_type": "Source",
        	"filename": "123.xml",
        	"filesize": 900
      	}
    	]
  	}
	]
  
	  

**Sample Response 1:** 

	[
  	{
    	"blob_id": "fbcc0e78-212a-4d3b-a28c-eb14678d35d2",
    	"error_code: 0
  	}
	]

**Code Example:** 
```
public Boolean CreateTopic(String topicName, String topicBody, String templeteType)
        {
            try
            {
                //create the topic
                topicUrl = String.Format("/v2/Projects/{0}/Outlines", _repo.Repository_id);
                apiUrlAction = String.Format("{0}{1}", _apiUrl, topicUrl);
                postData = _common.POSTTOPICDATA("RequestBodyExample.txt", bodyUploadResp.blob_id, topicName, dse.entity_id, templeteType);
                json = _common.POST(apiUrlAction, postData, "application/json;charset=utf-8");

                return true;
            }
            catch (Exception ex)
            {
                return false;
            }
        }
		
         public string POSTTOPICDATA(string _topicTemplete, string _blobId, string _topicName, string _entityId, string _templeteType)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(_topicTemplete))
                {
                    postData = sr.ReadToEnd();
                    postData = postData.Replace("blobIdToAdd", _blobId);
                    postData = postData.Replace("nameToAdd", _topicName);
                    postData = postData.Replace("parentIdToAdd", _entityId);
                    postData = postData.Replace("contentClassToAdd", _templeteType);
                }

                return postData;
            }
            catch (Exception ex)
            {
                return postData;
            }
        }
        
		public string POST(string _url, string _postData, string _contentType)
        {
            return REQUEST(_url, _postData, _contentType, "POST");
        }
		
		 private string REQUEST(string _url, string _postData, string _contentType, string requestType)
        {
            string json;
            HttpWebRequest request = WebRequest.Create(_url) as HttpWebRequest;
            request.Headers.Add(String.Format("TokenType: {0}", _TokenType));
            request.Headers.Add(String.Format("Authorization: {0}", _Athorization));
            request.ContentType = _contentType;
            request.Method = requestType;

            ASCIIEncoding encoding = new ASCIIEncoding();
            Byte[] byteArray = encoding.GetBytes(_postData);
            request.ContentLength = byteArray.Length;
            using (var Stream = request.GetRequestStream())
            {
                Stream.Write(byteArray, 0, byteArray.Length);
            }

            HttpWebResponse response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();
           
            using (StreamReader sr = new StreamReader(responseStream, true))//
            {
                json = sr.ReadToEnd();
            }
            responseStream.Close();
            response.Close();
            return json;
        }
```