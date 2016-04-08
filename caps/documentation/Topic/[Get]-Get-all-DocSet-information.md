---
title: [Get] Get all DocSet information
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b5f632cf-398e-4420-91fe-922d7b949ba3
---
# [Get] Get all DocSet information
**Description:** Get all DocSet info  

**API type:** GET

**URI:** v2/Projects/{ProjectID}/Docsets/{ContainID}/children?NextPageToken=&locale=default 

**Parameters:**  

	Project ID
	Contain ID
	 

**Note:** Project ID, Contain ID are required  

**Sample Request 1:** 

	Get https://caps-api-devint.azurewebsites.net/v2/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/Docsets/512975f2-0a97-4323-8c1c-db1aa6c8d833/children?NextPageToken=&locale=default  

**Sample Response 1:** 

	{
        "children": [
            {
                "entity_type": "Container",
                "name": "MRef_Test",
                "created_at": "2015-08-10T06:52:02Z",
                "created_by": "7cb0c87f-aad2-4334-a119-8c9c34802d41",
                "updated_at": "2015-08-21T06:31:50Z",
                "updated_by": "7cb0c87f-aad2-4334-a119-8c9c34802d41",
                "revision": 22,
                "class": "DocSet",
                "entity_class": "DocSet.MRef",
                "is_visible": true,
                "is_root": false,
                "has_children": true,
                "has_container": true,
                "is_deleted": false,
                "entity_id": "306737d2-d635-468b-8335-03a9291b6ee1",
                "locale": "en-US",
                "parent_id": "512975f2-0a97-4323-8c1c-db1aa6c8d833",
                "product_family": "BTS",
                "product_family_version": "100"
            },
  			{
                "entity_type": "Container",
                "name": "Test",
                "created_at": "2015-08-07T07:10:36Z",
                "created_by": "7cb0c87f-aad2-4334-a119-8c9c34802d41",
                "updated_at": "2015-08-24T06:52:10Z",
                "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",
                "revision": 25,
                "class": "DocSet",
                "entity_class": "Container",
                "is_visible": true,
                "is_root": false,
                "has_children": true,
                "has_container": true,
                "is_deleted": false,
                "entity_id": "85deb8e3-d698-4952-b025-e6e2a7b94c7b",
                "locale": "en-US",
                "parent_id": "512975f2-0a97-4323-8c1c-db1aa6c8d833",
                "community_content": false,
                "dcs_applies_to_product": "BBB",
                "dcs_applies_to_technology": "BBB",
                "dcs_applies_to_version": "BBB",
                "ipm": "7cb0c87f-aad2-4334-a119-8c9c34802d41",
                "is_auto_publish": false,
                "preferred_lib": "/library",
                "preferred_site_name": "MSDN",
                "product_family": "BTS",
                "product_family_version": "100",
                "stage_buildjob_id": "85deb8e3-d698-4952-b025-e6e2a7b94c7b--publish",
                "staged_locales": [
                    "en-US"
                ]
            }
	….
    }

**Code Example:** 
```
 private List<DocSet_Children> GetDocSets()
  {
            var docsetInfoLists = new List<DocSet_Children>();
            try
            {
                String docsetUrl = String.Format("/v2/Projects/{0}/Docsets/{1}/children?NextPageToken=&locale=default", _repo.repoInfo.entity_id, _repo.docSetsEntityID);

                //Get lists of docsets info
                var responseStream = common.GET(string.Format("{0}{1}", "https://caps-api-{0}.azurewebsites.net", docsetUrl));
                if (responseStream != null)
                {
                    using (StreamReader sr = new StreamReader((Stream)responseStream, true))
                    {
                        while (sr.Peek() >= 0)
                        {
                            string json = sr.ReadToEnd();
                            DocSet doInfoLists = JsonConvert.DeserializeObject<DocSet>(json);
                            docsetInfoLists = doInfoLists.children;
                        }
                    }

                    return docsetInfoLists;
                }
                return docsetInfoLists;
            }
            catch (Exception ex)
            {
                
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
		
    public class DocSet
    {
        public List<DocSet_Children> children { get; set; }
    }
	
	public class DocSet_Children
    {
        public string entity_id { get; set; }
        public string locale { get; set; }
        public bool is_deleted { get; set; }
        public int revision { get; set; }
        public string updated_by { get; set; }
        public string created_by { get; set; }
        public string parent_id { get; set; }
        public string default_locale { get; set; }
        public string entity_type { get; set; }
        public string name { get; set; }
    }
```