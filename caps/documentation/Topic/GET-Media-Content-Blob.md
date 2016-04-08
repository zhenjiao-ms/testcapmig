---
title: GET Media Content Blob
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 999a37d8-c423-4d90-a5bc-f168ee5cc443
---
# GET Media Content Blob
`<!--# Get Media Content Blob-->`

The URI format for fetching a **MediaContent** blob is:

GET _baseURI_`/v1/Projects/`_projectId_`/MediaContents/`_mediaId_`/Blobs?blobType=`_blobType_`&blobId=`_blobId_`&locale=`_locale_`&scale=`_scale_`&revision=`revision`&download=`_download_

Parameter | Required | Description
--- | :---: | ---
_baseUri_   | yes | Base api uri for the CAPS instance
_projectId_ | yes | Id of the project (portfolio)
_mediaId_   | yes | Id of the MediaContent item
_blobType_  | yes | One of `Source`, `Online`
_blobId_    | yes | Id of the blob
_locale_    | no  | Typically `en-US`
_scale_     | no  | One of (`small`,`full`). Use `small` to fetch a thumbnail image of the media.
_revision_  | no  | ??? Unknown if this parameter is useful. Presumably, it is the version of the content to retrieve.  Omitting this at least gets you the current version, which is most important right?
_download_  | no  | ??? Boolean value. This doesn't seem to make any difference in the results, whether it's true or false. 
<br/>
The returned content is marked `application/octet-stream` and contains the bytes of the media content.

### Example Code

The following sample code fragment provides a function that streams the media content (the image) to the provided `Stream`. This partial example presumes the `HttpClient` member has been initialized and the appropriate authorization headers have been set. 
 
```C#
private HttpClient _client;

public Task<HttpResponseMessage> GetAsync(string requestUri)
{
    return _client.GetAsync(requestUri);
}

public bool FetchMediaContentBlob(string baseUri, string projectId, string mediaContentId, string blobType, string blobId, Stream targetStream)
{
    string uri = string.Format("{0}/v1/Projects/{1}/MediaContents/{2}/Blobs?blobType={3}&blobId={4}&locale=en-US", 
        baseUri, projectId, mediaContentId, blobType, blobId);
    HttpResponseMessage response = this.GetAsync(uri).Result;
    if (null != response)
    {
        using (response)
        {
            if (response.IsSuccessStatusCode)
            {
                var task = response.Content.CopyToAsync(targetStream);
                task.Wait();
                return true;
            }
        }
    }
    return false;
}
```