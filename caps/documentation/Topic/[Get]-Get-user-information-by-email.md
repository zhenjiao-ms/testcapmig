---
title: [Get] Get user information by email
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8427c3a5-0c7e-4b81-a8d7-543a611c23c0
---
# [Get] Get user information by email
**Description:** Get user info by email

**API type:** GET

**URI:** v2/users?emails={emails} 

**Parameters:**  

	Emails 

**Note:**  

**Sample Request 1:** 

	Get https://caps-api-devint.azurewebsites.net/v2/users?emails=v-diluo@Microsoft.com  

**Sample Response 1:** 

	[  
	  {  
	    "department": "IXP",  
	    "id": "7cb0c87f-aad2-4334-a119-8c9c34802d41",  
	    "name": "Ding Luo (Beyondsoft Corporation)",  
	    "email": "v-diluo@microsoft.com",  
	    "alias": "v-diluo",  
	    "status": "active",  
	    "source_id": "7cb0c87f-aad2-4334-a119-8c9c34802d41",  
	    "source_type": "AAD",  
	    "type": "user",  
	    "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
	    "created_at": "2015-03-24T08:51:30.7176594Z",  
	    "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
	    "updated_at": "2015-03-24T08:51:30.7176594Z"  
	  }  
	]  
	
**Code Example:**
```
private Boolean GetEmails(String name)
{
string url = string.Format("https://caps-api-{0}.azurewebsites.net", TenantName) + string.Format("/v2/users?emails={0}", item.InnerText.Replace("\"", ""));
                            var GetToken = GET(url);
                            if (GetToken != null)
                            {
                                using (StreamReader sr1 = new StreamReader((Stream)GetToken, true))
                                {
                                    if (sr1.Peek() > 0)
                                    {
                                        string json1 = sr1.ReadToEnd();
                                        List<UserInfo> Tokeninfo = JsonConvert.DeserializeObject<List<UserInfo>>(json1);
                                        string User_ID = Tokeninfo[0].id.ToString();

                                       return true;
                                    }
                                }
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
							
	public class UserInfo 
	{
        public string id { get; set; }
        public string email { get; set; }
        public string name { get; set; }
    }					
```