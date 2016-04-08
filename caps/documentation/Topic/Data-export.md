---
title: Data export
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33856a7b-54eb-4994-890d-4e7dc32bbb0d
---
# Data export
##DataExportConsole - Dump anything from CAPS##
This tool is used to dump all data include metadata and blobs from CAPS, and it’s configurable user can specify which portfolio under which organization need to be dumped. Currently it does not support incremental export. It only exports the latest version of the assets. 

##How to run the tool##
###Configuration###
Before [running](#link2run) this tool to dump data from CAPS, the first step is to update the configuration file correctly.

There is a sample **.cfg** file named **sample\_localhost.cfg** under the tool path:

    {
      "service_url": "http://127.0.0.1/api/",
      "user": "access id",
      "key": "access key",
      "is_zip_content": false,
      "is_organization_name_as_file_name": true,
      "is_project_name_as_file_name": true,
      "is_container_name_as_file_name": true,
      "is_entity_name_as_file_name": false,
      "is_parallel": true,
      "is_dump_user_name": true,
      "batch_size": 500,
      "selection_pattern": "full",
      "organizations": [
        {
          "entity_id": "3d0479420e514aba857c28a8d5d9b238",
          "projects": [
            {
              "entity_id": "55889ff0-0943-4299-8e78-436bf911a3ac",
              "is_dump_all_blobs": false,
              "is_without_blobs": false,
              "is_dump_all_locales": false,
              "major_blob_types": [
                "Source",
                "Online"
              ],
              "entities": {
                "Article": []
              }
            }
          ]
        }
      ]
    }


####service\_url####
Indicates the endpoint of CAPS Service. In the sample it's pointed to the local, please update it up to the right destination. Below is the list of all CAPS Services:

- Sandbox https://caps-api-sandbox.azurewebsites.net/
- DevINT https://caps-api-devint.azurewebsites.net/
- PROD https://caps-api-prod.azurewebsites.net/

For example, if you want to connect to PROD environment please change it as following:

	"service_url": "https://caps-api-prod.azurewebsites.net/"


####user####
The access id of your account which will be used to login into CAPS service. 
Please [contact us](#link2contacts) to ask for the id of your account.

	
> **CAUTION: Don't share your id and key with others.**


####key####
The access key of your account. 
Please [contact us](#link2contacts) to ask for the account of your account.

> **CAUTION: Don't share your id and key with others.**


####is\_zip\_content####
Indicates whether zip the blobs or not. It will be much slower if enable this setting. 
Recommend value is **false**.

	"is_zip_content": false


####is\_organization\_name\_as\_file\_name####
Indicates whether use the name as the folder name or use the internal ID as the folder name for organization. 
Since the internal ID is not friendly for use, so consider to set it to **true**.

	"is_organization_name_as_file_name": true


####is\_project\_name\_as\_file\_name####
Indicates whether use the name as the folder name or use the internal ID as the folder name for portfolio.
Since the internal ID is not friendly for use, so consider to set it to **true**.

	"is_project_name_as_file_name": true


####is\_container\_name\_as\_file\_name####
Indicates whether use the name as the folder name or use the internal ID as the folder name for container.
Since the internal ID is not friendly for use, so consider to set it to **true**.

	"is_container_name_as_file_name": true


####is\_entity\_name\_as\_file\_name####
Indicates whether use the name as the file name or use the ID as the file name for Topic, Image and Token content.
Not like organization, portfolio and container, the ID of contents is global unique, so consider to set it to **false**.

	"is_entity_name_as_file_name": true


####is\_parallel####
Indicates whether let the tool raise multiple threads to parallel dump data from CAPS. Enable this will greatly improve the speed of dumping, so consider to set it to **true**.

	"is_parallel": true


####is\_dump\_user\_name####
Indicates whether replace any user fields in metadata or show the internal id of the user.
Recommend value is **true**.

	"is_dump_user_name": true


####batch\_size####
Indicates the batch size of the one dump action when running. Based on our testing the recommend value is 500.

	"batch_size": 500


####selection\_pattern####
Indicates how many metadata you want to get from CAPS, you can choose following patterns

- bulk
- summary
- full

The "bulk' is fastest and "full" is slowest, but as a dump tool the recommend value is "full".

	"selection_pattern": "full"


####organizations####
Indicates which organization you want to dump it, the value is an array and cannot be empty!

#####entity\_id#####
The internal ID of the organization. 

####projects####
Indicates which portfolio under the organization you want to dump it. All settings under this level are only affect this portfolio.

#####entity\_id#####
The internal ID of the portfolio.

#####is\_dump\_all\_blobs#####
Indicates whether dump all blobs belong to the content or not. There are lots of internal blobs in CAPS, it will be extremely slower if you set this to true, so th recommend value is **false**.

	"is_dump_all_blobs": "false"


#####is\_without\_blobs#####
Indicates whether dump blobs or not. if this setting is true then is\_dump\_all\_blobs will be lose effectiveness.
Default value is **false**.

	"is_without_blobs": "false"


#####is\_dump\_all\_locales#####
Indicates whether dump all locales data or only en-US.
Default value is **false**.

	"is_dump_all_locales": "false"


#####major\_blob\_types#####
Indicates which type of blob will be dumped. This is a multi-value settings. Typically we only aware 3 types:

- Source - Primary blob of Topic, Token and Image.
- Online - Primary blob of Image.
- Preview - HTML file of the Topic after building. 

Default value is **Source, Online**.

	"major_blob_types": [
            "Source",
            "Online"
          ]


#####entities#####
Indicates which type of content will be dumped. 
Leave it as empty to dump all content under this portfolio:

	"entities":{}


###<a name="link2run">Run</a>###
The command line is:

	Microsoft.Content.Service.DataExport.exe -c <config file for exporting> -t <the path which all data to be exported>


##How to download the tool##
###Binary###
\\\uafsall02\Public\CAPS-tools\DataExportConsole


##<a name="link2contacts">Contacts</a>##
For questions, please contact <a href="mailto:andxu@microsoft.com">Andy Xu</a> and cc <a href="mailto:jiqian@microsoft.com">Jingmin Qian</a>.
