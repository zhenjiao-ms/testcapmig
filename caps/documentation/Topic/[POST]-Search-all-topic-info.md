---
title: [POST] Search all topic info
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee2d3179-93e1-4f44-b5d3-f6c80181d075
---
# [POST] Search all topic info
**Description:**  Search all topic info
  

**API type:** POST

**URI:**  /{ProjectID}/Article/search?%24top=0&%24skip=2000
  

**Parameters:**  

	ProjectID
   
	  
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

    
 

**Note:** ProjectID is required, take 2000 articles in one search for performance

**Sample Request 1:** 

	POST https://caps-search-{0}.azurewebsites.net/6d36460d61a943d5ade70624086dcb41/Article/search?%24top=0&%24skip=3000 
	  
	Body:
    {
    "IsAnd": true,
    "Conditions": [
        {
            "metadata": "project_id",
            "operator": "EQ",
            "value": "{ProjectID}"
        },
        {
            "metadata": "locale",
            "operator": "EQ",
            "value": "en-US"
        },
        {
            "metadata": "outline_id",
            "operator": "UNDER",
            "value": "{OutlineID}"
        }
    ],
    "ConditionGroups": [],
    "Fields": [
        "entity_id",
        "name",
        "toc_title",
        "f1_keywords",
        "visible_index_keywords",
        "workflow_status",
        "assigned_to",
        "editor",
        "manager",
        "writer",
        "blob_updated_by",
        "blob_updated_at",
        "blob_checkout_by",
        "blob_checkout_at",
        "tags",
        "mref_comment_id",
        "mtps_api_name",
        "mref_subclass",
        "mtps_api_location",
        "updated_at_by_reflection",
        "mtps_api_type",
        "is_internal_only",
        "has_obsolete_api",
        "is_updated_by_reflection",
        "staged_message",
        "blob.source.content.revision",
        "blob.source.updated_at",
        "blob.source.updated_by",
        "blob.source.checkout_by",
        "parent_id",
        "parent_id",
        "source_id"
    ]
}



**Sample Response 1:** 

     {
    "total":191003,
    "data":[{
    "_id":"933fd679-87e5-442d-a485-d7020bde14da.fffff91d-bfd6-489a-8835-738 d56b55f65.en-us",
    "workflow_status":"Content Complete",
    "is_internal_only":false,
    "mref_comment_id":"M:System.Windows.Controls.Primitives.TextBoxBase.EndChange",
    "locale":"en-US",
    "blob.source.content.revision":55,
    "project_id":"933fd679-87e5-442d-a485-d7020bde14da",
    "is_updated_by_reflection":true,
    "mtps_api_type":"Assembly",
    "mref_subclass":"Member.Method",
    "has_obsolete_api":false,
    "blob.source.updated_at":"2015-07-09T11:52:11Z"
    …….}]
    } 




**Code Example:** 
```
     public List<QueryInfo> PublishToLive(string projectId)
    {
        try
        {
  List<QueryInfo> QueryInfoList=new List<QueryInfo>();
            string publishUrl = string.Format("/{ProjectID}/Article/search?%24top=0&%24skip=3000", projectId);
            string apiUrlAction =string.format("{0}{1}","https://caps-search-prod.azurewebsites.net" ,publishUrl);
            string postData = _common.POSTTOPICDATA("RequestBodyExample.txt");
           string json=POST(apiUrlAction,postData,"application/json;charset=utf-8");
 QueryResult repoInfoList = JsonConvert.DeserializeObject<QueryResult>(json);
                            if (repoInfoList.data.Count==0)
                            {
                                break;
                            }
                            foreach (QueryInfo item in repoInfoList.data)
                            {
                                QueryInfoList.Add(item);
                               // Console.WriteLine(item.entity_id);
                            }
Return QueryInfoList;

                   }
        catch (Exception ex)
        {
            // TODO: Log exception
            return false;
        }
    }
public string POSTTOPICDATA(string _topicTemplete)
        {
            string postData = "";
            try
            {
                using (StreamReader sr = new StreamReader(_topicTemplete))
                {
                    postData = sr.ReadToEnd();
                }
                return postData;
            }
            catch (Exception ex)
            {
                return postData;
            }
        }
public static string POST(string url, string body, string contentType)
    {
        return Request(url, body, contentType, "POST");
    }
public static string ResponseText(HttpWebRequest request, Encoding encoding)
    {
        using (HttpWebResponse response = request.GetResponse() as HttpWebResponse)
        {
            using (StreamReader sr = new StreamReader(response.GetResponseStream(), encoding))
            {
                return sr.ReadToEnd();
            }
        }
    }
private string Request(string url, string body, string contentType, string requestType)
    {
        HttpWebRequest request = WebRequest.Create(url) as HttpWebRequest;
        request.Headers.Add(string.Format("TokenType: {0}", _tokenType));
        request.Headers.Add(string.Format("Authorization: {0}", _authorization));
        request.ContentType = contentType;
        request.Method = requestType;
        TextRequestBody(request, body, Encoding.UTF8);
return ResponseText(request, Encoding.UTF8);
    }

 public class QueryResult
    {
        public List<QueryInfo> data { get; set; }
    }
    public class QueryInfo
    {
        public string entity_id { get; set; }
        public string name { get; set; }
        public string parent_id { get; set; }
    }

  
```