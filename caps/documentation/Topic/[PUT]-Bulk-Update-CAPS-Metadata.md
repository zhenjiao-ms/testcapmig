---
title: [PUT] Bulk Update CAPS Metadata
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd54baed-4a51-4fc4-a093-b5324d60f9f9
---
# [PUT] Bulk Update CAPS Metadata
**Description:** Bulk Update CAPS Metadata (Toc General and Publish)

**API type:** PUT

**URI:** v2/Projects/{projectID}/EntityJob/Article

**Parameters:**  

	ProjectId  
    
    Request body:
    {
    "locale": {locale},
    "job_type": "BatchUpdate",
    "include_entity_ids": [
        {GUID}
    ],
    "mode": "Auto",
    "extra": {
        "changes": {
        },
        "delta_changes": 
		{
		}
    },
    "fields": [
    ]
    }


	
**Note:**  ProjectId is required.
  
**Sample Request 1:** 

	GET https://caps-api-devint.azurewebsites.net/v2/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/EntityJob/Article
    Body:
     {
    "locale": "en-US",
    "job_type": "BatchUpdate",
    "include_entity_ids": [
        "7d74e894-7225-46d8-b868-4c0ec821194f","9c4f6fab-1f20-4348-b9bb-10359a720c86","b721c5b1-0cda-4da5-8f49-5e2daa69ad97","52821297-7008-442d-9aca-b73ccd2cfbb8","a03e3a69-7751-4658-8490-1eb4853f1662","d300f4a7-84bd-4678-9a5d-177b672dc925","b9b885c3-3136-428d-8ea7-2bf01e8c9aca","f2aeca9d-e0a2-43f1-8f68-771eea33c58a","9002ffca-229f-4c7f-9ed6-6fe7fd60235b","ed140236-821f-4c40-841a-7e16793b6030","14f10667-e491-4898-946d-ec4d35ea450d","23ae1753-8b6c-4670-9745-91b3a79b43d0","c13da574-cb2e-4769-aea2-634fa4431fdd","f5990a95-3470-4a8e-9e81-c41ff79c49d8","5881062e-be31-4cee-bf86-8c1ef2627bab","4b7c9bc4-b4b2-4124-b7e8-6dab562016fc","49926a62-5287-467a-993e-e31ae0ec5599","b50376b8-e43e-40cf-8a5b-36814958b9b2","6e54c717-30d0-4e28-8c5a-3d0970ba8e40","4090a08c-4aef-46f9-b2dd-6f9b7ce6ecdc"
    ],
    "mode": "Auto",
    "extra": {
        "changes": {
				 "ready_to_stage":true,"ready_to_promote":true,"publish_date":"2015-08-07","updated_date":"2015-08-07"
        },
        "delta_changes": 
		{
			
		}
    },
    "fields": [
    ]
}

**Sample Response 1:** 

    {
    "is_async": false,
    "result": {
        "Payload": {
            "error_code": 0,
            "project_id": "5deff363-2bde-473e-8479-ea9ce1c4a6bc",
            "job_id": "dummy job id",
            "user_name": "v-diluo@microsoft.com",
            "error_message": null,
            "context": "",
            "result": {
                "SuccessCount": 20
            }
        },
        "AssetId": "dummy job id",
        "Channel": "JobCompletion",
        "Event": "EntityJobComplete"
    },
    "error_code": 0
    }




**Code Example:** 
```
      public UpdateMetadataResult UpdateMetadata(string projectID,string tenantName)
        {
            try
            {
String url=string.format(" https://caps-api-{0}.azurewebsites.net/v2/Projects/{1}/EntityJob/Article",projectID,tenantName);
               // update the Meatadata, and return result
var responseStream = common.PUT(url, RepositoryID, "RequestBodyExample.txt", "application/json;charset=utf-8");
 UpdateMetadataResult Umr= new UpdateMetadataResult();  
  if (responseStream != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                    {
                        while (sr.Peek() >= 0)
                        {
                string json = sr.ReadToEnd();
              Umr=JsonConvert.DeserializeObject<UpdateMetadataResult>(json);
                 }
                    }
                        }
                        return Umr;
            catch (Exception Ex)
            {
                return Ex.ToString();
            }
        }
public object PUT(string _url, string _postData, string _contentType)
        {
            System.GC.Collect();
            HttpWebRequest request = WebRequest.Create(_url) as HttpWebRequest;
            request.Headers.Add(String.Format("TokenType: {0}", "jwt"));
            request.Headers.Add(String.Format("Authorization: {0}", "Authorization"));
            request.ContentType = _contentType;
            request.Method = "PUT";
            request.Timeout = "300000";
ASCIIEncoding encoding = new ASCIIEncoding();
            Byte[] byteArray = encoding.GetBytes(_postData);
            request.ContentLength = byteArray.Length;
            using (var Stream = request.GetRequestStream())
            {
                Stream.Write(byteArray, 0, byteArray.Length);
            }
HttpWebResponse response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();
            return responseStream;
        }
 public class UpdateMetadataResult
    {
        public UpdateResult result { get; set; }
    }

    /// <summary>
    /// Used to deserialize the JSON in the HTTP response body 
    /// for result information of updating metadata.
    /// </summary>
    public class UpdateResult
    {
        public PayloadResult Payload { get; set; }
    }

    /// <summary>
    /// Used to deserialize the JSON in the HTTP response body 
    /// for payload result information of updating metadata.
    /// </summary>
    public class PayloadResult
    {
        public string error_code { get; set; }
        public string user_name { get; set; }
        public string error_message { get; set; }
        public ResultCount result { get; set; }
    }

    /// <summary>
    /// Used to deserialize the JSON in the HTTP response body 
    /// for successful number of updating metadata.
    /// </summary>
    public class ResultCount
    {
        public int SuccessCount { get; set; }
    }

```