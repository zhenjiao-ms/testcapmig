---
title: [Get] Get the Containers by DocSet id(Toc, NotInToc, PaveOver)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b4d8170-878e-49e9-ae0f-e24e06f8632d
---
# [Get] Get the Containers by DocSet id(Toc, NotInToc, PaveOver)

**Description:** Get the containers by DocSet Id, it contains Toc, Not In Toc and Retired Content  

**API type:** GET

**URI:** v1/Projects/{ProjectID}/Containers/{ContainerID}:(children(container))  

**Parameters:**  

	ProjectID
	ContainerID  

**Note:** N/A  

**Sample Request 1:** 

	Get https://caps-api-devint.azurewebsites.net/v1/Projects/05f57908-75ce-4769-bd3d-1528c9cba379/Containers/3057cc13-8d65-45fe-9403-4d8b212cb31f:(children(container))  
   
**Sample Response 1:** 

	[  
	  {  
	    "children": [  
	      {  
	         "entity_type": "Container",  
	         "name": "PaveOver",  
	         "created_at": "2015-08-04T07:40:02Z",  
	         "created_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "updated_at": "2015-08-04T07:40:02Z",  
	         "updated_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "revision": 1,  
	         "class": "PaveOver",  
	         "entity_class": "Container",  
	         "is_visible": true,  
	         "is_root": false,  
	         "url": "https://caps-api-devint.azurewebsites.net/v1/projects/05f57908-75ce-4769-bd3d-1528c9cba379/containers/88b5d845-da49-48c2-a8ae-0c09e72a8d2c",  
	         "has_children": false,  
	         "has_container": false,  
	         "is_deleted": false,  
	         "entity_id": "88b5d845-da49-48c2-a8ae-0c09e72a8d2c",  
	         "locale": "en-US",  
	         "parent_id": "3057cc13-8d65-45fe-9403-4d8b212cb31f",  
	         "preferred_site_name": "MSDN",  
	         "preferred_lib": "/library",  
	         "is_auto_publish": false  
	      },  
	      {  
	         "entity_type": "Container",  
	         "name": "NotInToc",  
	         "created_at": "2015-08-04T07:40:02Z",  
	         "created_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "updated_at": "2015-08-04T07:40:02Z",  
	         "updated_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "revision": 1,  
	         "class": "NotInToc",  
	         "entity_class": "Container",  
	         "is_visible": true,  
	         "is_root": false,  
	         "url": "https://caps-api-devint.azurewebsites.net/v1/projects/05f57908-75ce-4769-bd3d-1528c9cba379/containers/9df72662-e512-42b1-a9db-df4a6fdb5e42",  
	         "has_children": false,  
	         "has_container": false,  
	         "is_deleted": false,  
	         "entity_id": "9df72662-e512-42b1-a9db-df4a6fdb5e42",  
	         "locale": "en-US",  
	         "parent_id": "3057cc13-8d65-45fe-9403-4d8b212cb31f",  
	         "preferred_site_name": "MSDN",  
	         "preferred_lib": "/library",  
	         "is_auto_publish": false  
	      },  
	      {  
	         "entity_type": "Container",  
	         "name": "Toc",  
	         "created_at": "2015-08-04T07:40:02Z",  
	         "created_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "updated_at": "2015-08-04T07:40:02Z",  
	         "updated_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	         "revision": 1,  
	         "class": "Toc",  
	         "entity_class": "Container",  
	         "is_visible": true,  
	         "is_root": false,  
	         "url": "https://caps-api-devint.azurewebsites.net/v1/projects/05f57908-75ce-4769-bd3d-1528c9cba379/containers/d4515d52-0944-4927-8323-58caeb53a83b",  
	         "has_children": true,  
	         "has_container": false,  
	         "is_deleted": false,  
	         "entity_id": "d4515d52-0944-4927-8323-58caeb53a83b",  
	         "locale": "en-US",  
	         "parent_id": "3057cc13-8d65-45fe-9403-4d8b212cb31f",  
	         "preferred_site_name": "MSDN",  
	         "preferred_lib": "/library",  
	         "is_auto_publish": false  
	      }  
	    ],  
	    "metadata_url": "https://caps-api-devint.azurewebsites.net/v1/projects/05f57908-75ce-4769-bd3d-1528c9cba379/containers/3057cc13-8d65-45fe-9403-4d8b212cb31f:(metadata)",  
	        "children_url": "https://caps-api-devint.azurewebsites.net/v1/projects/05f57908-75ce-4769-bd3d-1528c9cba379/containers/3057cc13-8d65-45fe-9403-4d8b212cb31f:(children)",  
	        "entity_id": "3057cc13-8d65-45fe-9403-4d8b212cb31f",  
	        "entity_type": "Container",  
	        "created_at": "2015-08-04T07:40:01Z",  
	        "created_by": "98327a30-7ae8-49b2-b881-7303a113c9ac",  
	        "updated_at": "2015-08-12T10:16:22Z",  
	        "updated_by": "7cb0c87f-aad2-4334-a119-8c9c34802d41",  
	        "metadata": {  
	          "class": "DocSet",  
	          "entity_class": "Container",  
	          "is_auto_publish": false,  
	          "is_visible": true,  
	          "name": "md_test",  
	          "preferred_lib": "/library",  
	          "preferred_site_name": "MSDN",  
	          "product_family": "BTS",  
	          "product_family_version": "100",  
	          "entity_type": "Container",  
	          "entity_id": "3057cc13-8d65-45fe-9403-4d8b212cb31f",  
	          "locale": "en-US",  
	          "updated_by": "7cb0c87f-aad2-4334-a119-8c9c34802d41",  
	          "updated_at": "2015-08-12T10:16:22Z",  
	          "revision": 6,  
	          "has_container": false,  
	          "is_deleted": false  
	        }  
	    }  
	]  
	
**Code Example:** 

```
private void GetDocSetTypeInfo(string DocsetURL, string proID, string tenant_id)
        {
		DocTypeURL = string.Format("https://caps-api-{0}.azurewebsites.net", _tenentName) + string.Format("/v1/Projects/{0}/Containers/{1}:(children(container))", _repo.repoInfo.entity_id, item.entity_id);
            var GetDocInfo = common.GET(DocsetURL);
            if (GetDocInfo != null)
            {
                using (StreamReader sr = new StreamReader((Stream)GetDocInfo, true))
                {
                    while (sr.Peek() >= 0)
                    {
                        string json = sr.ReadToEnd();

                        List<DocTypeInfo> repoInfoList = JsonConvert.DeserializeObject<List<DocTypeInfo>>(json);

                    }
                }
            }
        }
		
		public object GET(string _url)
        {
            HttpWebRequest request = WebRequest.Create(_url) as HttpWebRequest;
            request.Headers.Add(String.Format("TokenType: {0}", "jwt"));
            request.Headers.Add(String.Format("Authorization: {0}", "Authorization"));
            request.ContentType = _contentType;
            request.Method = "GET";
            request.Timeout = "300000";

            var response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();
            return responseStream;
        }
		
	public class DocTypeInfo
    {
        public List<DocSetTypeInfo> children { get; set; }
    }

    public class DocSetTypeInfo
    {
        public String name { get; set; }
        public String entity_id { get; set; }
        public String parent_id { get; set; }
        public String has_children { get; set; }
        public String has_container { get; set; }
    }
```