---
title: [POST] Update content into blobs by blob id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a00a06be-1e2f-4f6e-8a2f-2cd4e3677eab
---
# [POST] Update content into blobs by blob id
**Description:** Updata Content by blob id

**API type:** POST

**URI:** v1/Projects/{projectid}/TempFiles?tempFileId={blobid}&locale=en-US

**Parameters:**  

	ProjectId  
	BlobId
	
	-----------------------------7df25d1330476  
	Content-Disposition: form-data; name="BlobData"  
	…  
	Content  
	…  
	-----------------------------7df25d1330476--  
	  
**Note:**  

	Contenttype: multipart/form-data; boundary=---------------------------7df25d1330476  

  
**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/TempFiles?tempFileId=9050fd5d-7091-488c-8aca-918218cef637&locale=en-US

**Sample Response 1:** 

    "ddb686e5-249e-4372-8af6-d3f5a4f3675c"
 
	

**Code Example:** 
```
private Boolean Update(String topicBody,String entityId, String blobId)
        {
            try
            {
                String apiurl = String.Format("https://caps-api-{0}.azurewebsites.net", _tenentName);
                String topicUrl = String.Format("/v1/Projects/{0}/TempFiles?tempFileId={1}&locale=en-US", _pro, blobId);
                String apiUrlAction = String.Format("{0}{1}", apiurl, topicUrl);
                topicBody = String.Format(MLCapsImportConstants.TOPICBODYTEMPLATE, topicBody);

                String postData = String.Concat( "-----------------------------7df25d1330476\x0d\x0a", "Content-Disposition: form-data; name=\"BlobData\"\x0d\x0a","<?xml version='1.0' encoding='utf-8'?>", topicBody, "\x0d\x0a-----------------------------7df25d1330476--\x0d\x0a");
                string json = common.POST(apiUrlAction, postData, "multipart/form-data; boundary=---------------------------7df25d1330476");

                using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                {
                    string json = sr.ReadToEnd();
                }
                return true;
            }
            catch(Exception ex)
            {
                // TODO: Log exception
                return false;
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
            request.Headers.Add(String.Format("Authorization: {0}", _Athorization));
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