---
title: [GET] Get all organization
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee87928c-5f68-4fc9-a25d-f3f93687c0b5
---
# [GET] Get all organization
**Description:** Get all organization info  

**API type:** GET

**URI:** v1/Organizations

**Parameters:**  

	N/A
	 
**Note:**   

**Sample Request 1:** 

	Get  https://caps-api-devint.azurewebsites.net/v1/Organizations

**Sample Response 1:** 

	[
  
    {
    "metadata_url": "https://caps-api-devint.azurewebsites.net/v1/organizations/ffabd50649854ead8b30a42798aeb2ed:(metadata)",
    "children_url": "https://caps-api-devint.azurewebsites.net/v1/organizations/ffabd50649854ead8b30a42798aeb2ed:(children)",
    "entity_id": "ffabd50649854ead8b30a42798aeb2ed",
    "entity_type": "Organization",
    "created_at": "2014-07-30T03:34:01.9482389Z",
    "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",
    "updated_at": "2014-07-30T03:34:01.9482389Z",
    "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",
    "metadata": {
      "name": "partner",
      "entity_type": "Organization",
      "default_locale": null,
      "locale": null,
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",
      "created_at": "2014-07-30T03:34:01.9482389Z",
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",
      "updated_at": "2014-07-30T03:34:01.9482389Z"
    }
    }
    ….
    ]


**Code Example:** 
```
 public void GetRepositoryInfo()
        {
            try
           {
                //Get all RepositoryName APIurl
               RepositoryURL = string.Format("https://caps-api-{0}.azurewebsites.net", Program.TENANTNAME) + "/v1/Organizations";
                //Get resurn sult
                var GetFortfoilo = common.GET(RepositoryURL);
                if (GetFortfoilo != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)GetFortfoilo, true))
                    {
                        if (sr.Peek() >= 0)
                        {
                            string json = sr.ReadToEnd();
                            //Convert to "RepositoryInfo" object
                            List<RepositoryInfo> repoInfoList = JsonConvert.DeserializeObject<List<RepositoryInfo>>(json);
                        }
                    }
                }
            }
            catch (Exception ex)
            {
                throw;
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
		
    public class RepositoryInfo
    {
        public string entity_id { get; set; }
        public tenInfo metadata { get; set; }
    }
    
    public class tenInfo 
    {
        public string name { get; set; }
    }
```