---
title: Getting Started with CAPS API
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 359d0058-0236-4dd9-9398-c8545a10843b
---
# Getting Started with CAPS API


To ask the permission, please mail to csicapsperms@microsoft.com 


parameter   |Description  
--------- |---------
User      |  Ask permission 
Token Type|usually jwt or sas





Here is the code to get the organization IDs with CAPS API
```
        public class RepositoryInfo
        {
            public string entity_id { get; set; }
        }
    
        public static List<string> GetOrganizationID()
        {
            List<string> IDs = new List<string>();

            string user = "v-yichen@microsoft.com";
            string tokenType = "jwt";
            String URL = @"https://caps-api-prod.azurewebsites.net/v1/Organizations"; //The URL of CAP API


            HttpWebRequest request = WebRequest.Create(URL) as HttpWebRequest;
            request.Headers.Add(String.Format("Authorization: {0}", user));
            request.Headers.Add(String.Format("TokenType: {0}", tokenType));
            request.Headers.Add("X-CAPS-PageSize: 0");
            request.ContentType = "application/json;charset=utf-8";
            request.Method = "GET";
            var response = request.GetResponse() as HttpWebResponse;
            var responseStream = response.GetResponseStream();

            //Deserialize Json file
            using (StreamReader sr = new StreamReader((Stream)responseStream, true))
            {
                List<RepositoryInfo> repoInfoList = null;

                if (sr.Peek() >= 0)
                {
                    string json = sr.ReadToEnd();

                    //Convert to "RepositoryInfo" object
                    repoInfoList = JsonConvert.DeserializeObject<List<RepositoryInfo>>(json);
                }

                foreach (RepositoryInfo item in repoInfoList)
                {
                    IDs.Add(item.entity_id);
                }
            }
            return IDs;
        }    

```
