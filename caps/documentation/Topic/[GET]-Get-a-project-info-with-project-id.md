---
title: [GET] Get a project info with project id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a64b1cdc-f468-442b-b90c-1c54d42d8e6c
---
# [GET] Get a project info with project id
**Description:** Get a project info with project id  

**API type:** GET

**URI:** /v1/Projects/{ProjectId}:(children(container))

**Parameters:**  

	ProjectId
	 
**Note:**   

**Sample Request 1:** 

	Get  https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377:(children(container)) 

**Sample Response 1:** 

	[
    {
    "metadata_url": "https://caps-api-devint.azurewebsites.net/v1/projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377:(metadata)",
    "children_url": "https://caps-api-devint.azurewebsites.net/v1/projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377:(children)",
    "entity_id": "60202b11-04dc-4e03-a0b5-9bc2c39a8377",
    "entity_type": "Project",
    "parent_id": "ffabd50649854ead8b30a42798aeb2ed",
    "created_at": "2015-03-11T01:59:51.1498963Z",
    "created_by": "afb4736e-f853-49db-b42c-db391da18e9e",
    "updated_at": "2015-03-11T01:59:51.1498963Z",
    "updated_by": "afb4736e-f853-49db-b42c-db391da18e9e",
    "metadata": {
      "name": "Yingda.Test"
    }
    }
    ]

**Code Example:** 
```
 private Boolean GetDocsetsInfo()
        {
        String _apiUrl= String.Format(https://caps-api-{0}.azurewebsites.net, Configuration.TENANTNAME);"
        String _docsetUrl = String.Format("/v1/Projects/{0}:(children(container))", repoInfo.entity_id);
            //get docset info if matched
            var responseStream = common.GET(string.Format("{0}{1}", _apiUrl, _docsetUrl));
            if (responseStream != null)
            {
                using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                {
                    while (sr.Peek() >= 0)
                    {
                        string json = sr.ReadToEnd();
                        conInfoList=JsonConvert.DeserializeObject<List<ContainerInfo>>(json);
                    }
                }
                
            return true;
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
		
    public class ContainerInfo
    {
        public List<Container_Children> children { get; set; }
    }

    public class Container_Children
    {
        public string entity_id { get; set; }
        public string name { get; set; }
        public string url { get; set; }
        public bool has_children { get; set; }
        public bool has_Container { get; set; }
        public string parent_id { get; set; }
    }
```