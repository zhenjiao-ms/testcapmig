---
title: [GET] Get publish state info by bulidjobid
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dee48eb4-d752-4d20-979d-15482a38dd77
---
# [GET] Get publish state info by bulidjobid
**Description:** Get publish state info by bulidjobid

**API type:** GET

**URI:** v1/Projects/{Projectid}/BuildJobs/{bulidjobid}/properties?locale={locale}

**Parameters:**  

	ProjectId  
	bulidjobid
    locale

	
**Note:**  ProjectId and bulidjobid,locale are required.
  
**Sample Request 1:** 

	GET https://caps-api-devint.azurewebsites.net/v1/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/BuildJobs/da180f8a-6d2e-4c09-88e5-da8372be2936--promote/properties?locale=en-US 
 

**Sample Response 1:** 

    {
      "job_status": "Succeeded",
      "is_incremental": false,
      "is_on_demand": true,
      "is_scheduled": null,
      "message": "Succeeded in 00:00:08.3037704 seconds.",
      "triggered_by": "v-diluo@microsoft.com",
      "started_at": "2015-10-20T05:38:05.7249287+00:00",
      "ended_at": "2015-10-20T05:38:13.9064588+00:00",
      "cancelable": false,
      "total_count": 10,
      "successful_count": 10,
      "failed_count": 0,
      "job_progress": 1,
      "source_entities": [
    "{\"project_id\":\"5deff363-2bde-473e-8479-ea9ce1c4a6bc\",\"entity_id\":\"da180f8a-6d2e-4c09-88e5-da8372be2936\",\"entity_type\":\"Container\",\"locale\":\"en-US\"}"
     ],
      "latest_blob_id": "8587562874004887117",
      "categorized_count": "{\"Outline\":{\"total_count\":3,\"successful_count\":3,\"failed_count\":0},\"Article\":{\"total_count\":7,\"successful_count\":7,\"failed_count\":0}}",
      "job_type": "Live",
      "job_level": "DocSet",
      "staged_locales": null,
      "promoted_locales": null,
      "locales": [
    "en-US"
      ],
      "entity_id": "da180f8a-6d2e-4c09-88e5-da8372be2936--promote",
      "project_id": "5deff363-2bde-473e-8479-ea9ce1c4a6bc",
      "parent_id": "66216db2-b1c1-4036-8d0a-d624f0d932f3",
      "organization_id": "ffabd50649854ead8b30a42798aeb2ed",
      "name": null,
      "revision": 145,
      "locale": "en-US",
      "default_locale": "en-US",
      "entity_type": "BuildJob",
      "assigned_to": null,
      "created_at": "2015-08-28T02:03:03Z",
      "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",
      "attributes": null,
      "readonly_fields": null,
      "e_tag": "W/\"datetime'2015-10-20T05%3A38%3A13.2311349Z'\"",
      "group_revisions": {
    "Localizable": 0
      }
    }



**Code Example:** 
```
private PublishStatusInfo GetPublishStatus(string projectId, string buildJobId, string locale)
  {
            var publishStatusInfo = new PublishStatusInfo();
            try
            {
                String getstatusUrl = String.Format("/v1/Projects/{Projectid}/BuildJobs/{bulidjobid}/properties?locale={locale}", projectId,buildJobId,locale);

                //Get Publish Status info
                var responseStream = common.GET(string.Format("{0}{1}", "https://caps-api-{0}.azurewebsites.net", getstatusUrl));
                if (responseStream != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                    {
                        while (sr.Peek() >= 0)
                        {
                            string json = sr.ReadToEnd();
                            publishStatusInfo = JsonConvert.DeserializeObject<DocPublishStatusInfoSet>(json);
                
                        }
                    }

                 
                }
                return publishStatusInfo;
            }
            catch (Exception ex)
            {
                thow;
            }
    }
		
	public object GET(string _url)
    {
            HttpWebRequest request = WebRequest.Create(_url) as HttpWebRequest;
            request.Headers.Add(String.Format("Authorization: {0}", Authorization));
            request.Headers.Add(String.Format("TokenType: {0}", TokenType));
            request.ContentType = _contentType;
            request.Method = "GET";

            var response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();
            return responseStream;
     }
	
    public class PublishStatusInfo
     {
        [JsonProperty(PropertyName = "job_status")]
        public string job_status { get; set; }
        [JsonProperty(PropertyName = "message")]
        public string message { get; set; }
        [JsonProperty(PropertyName = "total_count")]
        public string total_count { get; set; }
        [JsonProperty(PropertyName = "successful_count")]
        public string successful_count { get; set; }
        [JsonProperty(PropertyName = "failed_count")]
        public string failed_count { get; set; }
        [JsonProperty(PropertyName = "job_progress")]
        public string job_progress { get; set; }
        [JsonProperty(PropertyName = "latest_blob_id")]
        public string latest_blob_id { get; set; }
        [JsonProperty(PropertyName = "job_type")]
        public string job_type { get; set; }
        [JsonProperty(PropertyName = "job_level")]
        public string job_level { get; set; }
        [JsonProperty(PropertyName = "entity_id")]
        public string entity_id { get; set; }
        
    } 
```