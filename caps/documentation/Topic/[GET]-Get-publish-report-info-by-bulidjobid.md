---
title: [GET] Get publish report info by bulidjobid
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46836b93-28c3-4ddc-84f5-a46a02576797
---
# [GET] Get publish report info by bulidjobid
**Description:** Get publish report info by bulidjobid

**API type:** GET

**URI:** /v2/Projects/{ProjectID}/Entities/{EntitiesID}/blobs/Report?blobId={Bulidjob }&locale={LOCALE}

**Parameters:**  

	ProjectId  
    EntitiesID
	bulidjobid
    locale

	
**Note:**  ProjectId,EntitiesID,bulidjobid,locale are required.
  
**Sample Request 1:** 

	GET https://caps-api-devint.azurewebsites.net/v1/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/BuildJobs/da180f8a-6d2e-4c09-88e5-da8372be2936--promote/report?locale=en-US 
  

**Sample Response 1:** 
```
 blob_url=https://x3capscrpartnerint.blob.core.windows.net/5deff363-2bde-473e-8479-ea9ce1c4a6bc/8587515317492404207:en-US?snapshot=2015-12-14T06:40:22.8417927Z&sv=2014-02-14&sr=b&sig=KSKp7c%2FUviascRG77YXY5097PQFp%2B3rh98lY0NCNJJI%3D&st=2015-12-14T06%3A38%3A38Z&se=2015-12-14T07%3A43%3A38Z&sp=r

```

**Code Example:** 
```
private string GetPublishReport(string projectId, string buildJobId, string locale)
  {
  string report=null;
            try
            {
                String getreportUrl = String.Format("/v1/Projects/{projectId}/BuildJobs/{buildJobId}/report?locale={locale}", projectId,buildJobId,locale);

                //Get Publish Status info
                var responseStream = common.GET(string.Format("{0}{1}", "https://caps-api-{0}.azurewebsites.net", getreportUrl));
                if (responseStream != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                    {
                        while (sr.Peek() >= 0)
                        {
                           report = sr.ReadToEnd();
                        }
                    }

                 
                }
                return report;
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
		
   
	
```