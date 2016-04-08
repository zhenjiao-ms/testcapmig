---
title: Media Content
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd334bbd-490d-47b4-b736-d6a05ec56309
---
# Media Content
# Media Content

Media Content (A.K.A. images) is stored in a flat container. There is no hierarchy or TOC for Media Content. For each media item there is one and only one blob with the type `Online`. Any additional blobs for the media item are designated as `Source`. Using the API you can fetch the image file, and also a thumbnail of of the image.

The Alt Text for an image is available as an attribute in the json for the item.

To see all the Media Content in your project:

1. Get the project id of the container with class `MediaContent`
2. Enumerate the children of this container. For a small number of images, this can be done in one shot using the route `v1/Projects/`_projectID_`/Containers/`_mediaContainerId_`:(children)`, or in paged fashion using the route `v1/Projects/`_projectID_`/Containers/`_mediaContainerId_`/Children?locale=en-US&pageSize=`_count_`&pageToken=`_token_.

Each child is a media content item. 

## Example JSON for Media Content Item
The alt text for the image is in the `alternate_text` attribute. This example item carries three files: a GIF, two PNGs and the orginal master file, which is an SVG. The GIF has been designated the `Online` file.

```json
{
  "entity_type": "MediaContent",
  "name": "CTAS Logo",
  "assigned_to": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "workflow_status": "Complete",
  "created_at": "2015-09-16T20:04:04Z",
  "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "updated_at": "2015-10-27T19:49:51Z",
  "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "revision": 5,
  "content_class": "Icon",
  "is_visible": true,
  "is_root": false,
  "blob_id": "9fa8fba7-dd82-425f-9d05-2169ae778d75",
  "blob_type": "Online",
  "blob_revision": 1,
  "blob_created_at": "2015-09-16T20:05:09Z",
  "blob_created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "blob_updated_at": "2015-09-16T20:05:09Z",
  "blob_updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/mediacontents/c2e36d08-236b-4b21-a393-8afcf6859d4c",
  "media_content_online_image_thumbnail_url": "https://caps-api-devint.azurewebsites.net/v1/projects/13027dce-db77-476b-8c34-4154e3445fff/mediacontents/c2e36d08-236b-4b21-a393-8afcf6859d4c:(blobcontent(Online))?locale=en-US&scale=small",
  "has_children": false,
  "has_container": false,
  "is_deleted": false,
  "blobs": [
    {
      "blob_id": "9fa8fba7-dd82-425f-9d05-2169ae778d75",
      "created_at": "2015-09-16T20:05:09Z",
      "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "updated_at": "2015-09-16T20:05:09Z",
      "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "revision": 1,
      "blob_type": "Online",
      "filename": "NewLogo.gif",
      "filesize": 982,
      "word_count": 0
    },
    {
      "blob_id": "3aa38bb6-41c1-44bd-b2b3-7464a3919127",
      "created_at": "2015-10-27T20:44:08Z",
      "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "updated_at": "2015-10-27T20:44:08Z",
      "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "revision": 1,
      "blob_type": "Source",
      "filename": "NewLogoDark.png",
      "filesize": 1744,
      "word_count": 0
    },
    {
      "blob_id": "8615ad77-a61c-40eb-ac83-fea30a33e1ac",
      "created_at": "2015-09-16T20:04:04Z",
      "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "updated_at": "2015-09-16T20:04:04Z",
      "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "revision": 1,
      "blob_type": "Source",
      "filename": "CTASLogo.svg",
      "filesize": 1294,
      "word_count": 0
    },
    {
      "blob_id": "f2b1dbbf-e17e-444d-9c6a-3cfaac93cc4e",
      "created_at": "2015-09-16T20:07:23Z",
      "created_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "updated_at": "2015-09-16T20:07:23Z",
      "updated_by": "d9af4dfa-fb56-443a-8fc6-376363f83610",
      "revision": 1,
      "blob_type": "Source",
      "filename": "NewLogo.png",
      "filesize": 2389,
      "word_count": 0
    }
  ],
  "entity_id": "c2e36d08-236b-4b21-a393-8afcf6859d4c",
  "locale": "en-US",
  "parent_id": "9247326d-6f32-4227-a096-1c5eabbb5875",
  "alternate_text": "CTAS Logo",
  "blob_need_handoff_locales": [
    "da-DK",
    "de-DE",
    "pt-BR",
    "zh-CN"
  ],
  "blob_no_need_handoff_locales": [],
  "designer": "d9af4dfa-fb56-443a-8fc6-376363f83610",
  "ht_target_locales": [
    "da-DK",
    "de-DE",
    "pt-BR",
    "zh-CN"
  ],
  "metadata_need_handoff_locales": [
    "da-DK",
    "de-DE",
    "pt-BR",
    "zh-CN"
  ],
  "mt_target_locales": [],
  "ready_for_localization": true,
  "requirement": "Master for this image is SVG."
}
```