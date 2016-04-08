---
title: [GET] Get an organization info by organization id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d4c9164-746c-47be-af02-ef7d3d8c2378
---
# [GET] Get an organization info by organization id
**Description:** Get an organziation info with organization id  

**API type:** GET

**URI:** v1/Organizations/{OrganizationId}/children?NextPageToken=&locale=default

**Parameters:**  

	OrganizationId
	 
**Note:**   

**Sample Request 1:** 

	Get  https://caps-api-devint.azurewebsites.net/v1/Organizations/ffabd50649854ead8b30a42798aeb2ed/children?NextPageToken=&locale=default

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
    ]   


**Code Example:** 
```

  public void GetPortfoiloInfo()
        {
        string DocsetURL = string.Format("https://caps-api-{0}.azurewebsites.net", Program.TENANTNAME) + string.Format("/v1/Organizations/{0}/children?NextPageToken=&locale=default", OrganizationId);
            var GetDocInfo = common.GET(DocsetURL);
            try
            {
                if (GetDocInfo != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)GetDocInfo, true))
                    {
                        if (sr.Peek() >= 0)
                        {
                            string json =headermark+sr.ReadToEnd()+footermark;
                            List<PortfolioInfo> repoInfoList = JsonConvert.DeserializeObject<List<PortfolioInfo>>(json);
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
		
    public class PortfolioInfo
    {
        public List<Portfolio_Children> children { get; set; }
    }
    
    public class Portfolio_Children
    {
        public string entity_id { get; set; }
        public string name { get; set; }
    }
```