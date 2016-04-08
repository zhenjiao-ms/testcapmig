---
title: Overview of Tokens
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46adf62d-612c-4c57-8b00-eff1f0fb3fa7
---
# Overview of Tokens
`<!-- # Overview of Tokens --> (TODO: remove literal when comments are allowed in md)`

Tokens are relatively simple to access in the CAPS API.

To access tokens, you need the usual project Id, and the id of the Project's Token container.

## Get the id for the project's Token container

Enumerate the children of the project:

`GET` *baseUri*`/v1/projects/`*projectId*`:(children)`

From the returned children, get the `entity_id` for the container with `"class": "Token"`. This is the project's Token container.

## Get the Token info

All tokens are children of the Token container.

`GET` *baseUri*`/v1/projects/`*projectId*`/Containers/`_tokenContainerId_`:(children)`

The JSON result adds the `"children"` array to the Token container information.

## Get Token info in paged fashion

To access all the tokens for a project with a large number of tokens, you should get the token info in paged fashion:

`GET` *baseUri*`/v1/projects/`*projectId*`/Tokens?`parentId=`_tokenContainerId_`&sortBy=`_fieldName_`&sortOrder=`asc|desc`&skip=`_count_`&take=`_count_`&selection=`full|summary`&locale=`_locale_

Parameter | Required | Description
--- | :---: | ---
baseUri   | yes | Base api uri for the CAPS instance
projectId | yes | Id of the project (portfolio)
parentId  | yes | Id of the project's Token container
sortBy    | no | Name of field whose value is used for ordering the results
sortOrder | no | One of (`asc`, `desc`). The ordering of the results, ascending, or descending, respectively.
skip      | yes | Number of items to skip
take      | yes | Maximum number of items to return
selection | no | How much detail to return. One of (`summary`, `full`), default: `summary`
locale    | no | Locale of token to return. _(?? PCD: not certain of meaning of the locale parameter)_ 

The response json is in the common paged group result format:
```
{
  "total_count": 2,
  "position": 0,
  "items": [
    {
    // contents of item
    },
    // ... additional items (if any)
  ]
}
```

The `total_count` value is the total number of available items, not the count of items returned. The `position` value should be the same as the `skip` parameter value. 

## Get the Token content

To get the definition of the token, get the Source blob content through the **Tokens** route:

`GET` *baseUri*`/v1/projects/`*projectId*`/Tokens/`_tokenId_`:(blobcontent(Source))`

## Example Token Info

The following example gets the tokens for a small project that has only two tokens.

```
GET https://caps-api-devint.azurewebsites.net/v1/Projects/13027dce-db77-476b-8c34-4154e3445fff/Containers/ce43d927-210b-45b6-99ca-e0838dd00a0c:(children)
```

#### Result
```
[
  {
    "children": [
      {
        "entity_type": "Token",
        "name": "Boilerplate",
        "created_at": "2015-10-08T21:00:37Z",
        "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "updated_at": "2015-10-08T21:40:30Z",
        "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "revision": 4,
        "content_class": "DDUE.Inline",
        "is_visible": true,
        "is_root": false,
        "blob_id": "daca3cc3-fcc5-4873-8655-c88c60c48b24",
        "blob_type": "Source",
        "blob_revision": 3,
        "blob_created_at": "2015-10-08T21:00:37Z",
        "blob_created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "blob_updated_at": "2015-10-08T21:04:28Z",
        "blob_updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/tokens/7dcbdc3c-5bf2-4994-8e82-71d1bb58fcdf",
        "has_children": false,
        "has_container": false,
        "is_deleted": false,
        "blobs": [
          {
            "blob_id": "daca3cc3-fcc5-4873-8655-c88c60c48b24",
            "created_at": "2015-10-08T21:00:37Z",
            "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
            "updated_at": "2015-10-08T21:04:28Z",
            "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
            "comments": "fix spelling",
            "revision": 3,
            "blob_type": "Source",
            "filename": "Boilerplate.xml",
            "filesize": 58,
            "word_count": 0
          }
        ],
        "entity_id": "7dcbdc3c-5bf2-4994-8e82-71d1bb58fcdf",
        "locale": "en-US",
        "parent_id": "ce43d927-210b-45b6-99ca-e0838dd00a0c",
        "blob_need_handoff_locales": [
          "de-DE",
          "fr-FR",
          "pt-BR",
          "zh-CN"
        ],
        "blob_no_need_handoff_locales": [],
        "ht_target_locales": [
          "de-DE",
          "fr-FR",
          "pt-BR",
          "zh-CN"
        ],
        "mt_target_locales": [],
        "ready_for_localization": true
      },
      {
        "entity_type": "Token",
        "name": "Generic",
        "created_at": "2015-09-16T20:10:19Z",
        "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "updated_at": "2015-09-16T20:11:46Z",
        "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "revision": 3,
        "content_class": "DDUE.Inline",
        "is_visible": true,
        "is_root": false,
        "blob_id": "74aa69c2-b821-43b6-bdd1-c2f3f4102eb8",
        "blob_type": "Source",
        "blob_revision": 2,
        "blob_created_at": "2015-09-16T20:10:19Z",
        "blob_created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "blob_updated_at": "2015-09-16T20:11:13Z",
        "blob_updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
        "url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/tokens/613f6390-ab3b-4f56-8bad-515be3bec37d",
        "has_children": false,
        "has_container": false,
        "is_deleted": false,
        "blobs": [
          {
            "blob_id": "74aa69c2-b821-43b6-bdd1-c2f3f4102eb8",
            "created_at": "2015-09-16T20:10:19Z",
            "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
            "updated_at": "2015-09-16T20:11:13Z",
            "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
            "comments": "create",
            "revision": 2,
            "blob_type": "Source",
            "filename": "Generic.xml",
            "filesize": 58,
            "word_count": 0
          }
        ],
        "entity_id": "613f6390-ab3b-4f56-8bad-515be3bec37d",
        "locale": "en-US",
        "parent_id": "ce43d927-210b-45b6-99ca-e0838dd00a0c",
        "blob_need_handoff_locales": [
          "de-DE",
          "en-US"
        ],
        "blob_no_need_handoff_locales": [],
        "ht_target_locales": [
          "de-DE",
          "en-US"
        ],
        "mt_target_locales": [],
        "ready_for_localization": true
      }
    ],
    "metadata_url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/containers/ce43d927-210b-45b6-99ca-e0838dd00a0c:(metadata)",
    "children_url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/containers/ce43d927-210b-45b6-99ca-e0838dd00a0c:(children)",
    "entity_id": "ce43d927-210b-45b6-99ca-e0838dd00a0c",
    "entity_type": "Container",
    "created_at": "2015-09-09T23:11:47Z",
    "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
    "updated_at": "2015-09-09T23:11:47Z",
    "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
    "metadata": {
      "is_visible": true,
      "class": "Token",
      "name": "Token",
      "entity_type": "Container",
      "entity_id": "ce43d927-210b-45b6-99ca-e0838dd00a0c",
      "locale": "en-US",
      "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "updated_at": "2015-09-09T23:11:47Z",
      "revision": 1,
      "has_container": false,
      "is_deleted": false,
      "entity_class": "Container"
    }
  }
]
```