---
title: Understanding publishing errors and warning messages
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 183fe29d-2c32-44d8-aae6-98ff35304514
---
# Understanding publishing errors and warning messages
The following table describes what a publishing error or warning is and  when an issue is considered an error or a warning during publishing.

## Definitions

-   Publishing error:  The issue prevents the topic from publishing. Some errors prevent the topic to be published with a missing content to prevent customers no to accomplish the task described in the topic.

-   Warning: The issue does not prevent the topic from publishing. However, the topic has problems that might affect the customer experience

## Errors

|Issue|Reason for error category|
|---------|-----------------------------|
|Broken  image|Missing important data. In the case of steps, not having the art will make very difficult for customers to follow up the numbered steps.|
|Broken link|Missing important data.  Not having the token will make the content unreadable as full sentences are missing, product names, or other key content in the middle of the sentences.|
|Topic cannot be published to live because it has not been published to stage yet.|You always need to publish the topic to stage before going live. It is two actions.|
|A child node in the docset references another docset or an external topic that cannot be published.|There is an error with the reference project so publishing is prevented to avoid a broken experienced to the user.|
|Mandatory publishing metadata is not set.|Some metadata, like some ms.xxx attributes is mandatory and need to be set before we can published.|
|Localized version is higher than English|Localized version cannot be higher than English when publishing. This is to prevent releasing content that is not ready for external users to consume.|
|Having multiple root nodes in docset is not supported for offline files.|We do not support this scenario today, So the offline file cannot be created.|
|Retired topic cannot be published to stage/live. There might may referenced in another docset.|The content is shared and you will need to remove the sharing before you can retire. This is to avoid that content shows in the TOC that is no longer valid.|
|The topic has been published already with a different product family.|We cannot publish a  project into multiple product families. You will need to do a product family migration before you can publish into this other product family.|

## Warnings

|Issue|Reason for warning category|
|---------|-------------------------------|
|Broken link to a topic|Usually a link is added for additional or related information on the topic. Not having the link in the topic does not prevent the readability of the content. It degrades customer experience though.|
|Broken bookmark|Usually a link is added for additional or related information on the topic. Not having the link in the topic does not prevent the readability of the content. It degrades customer experience though.|
|Broken code reference|Missing important data.  Not having the code snippet will make hard for the user to follow the rest of the section or topic as most likely is related to that snippet.|
|User tries to publish  topics for a language that do not exist for that language.|MTPS will default the users to the English content within the localized library. Therefore, CAPS will return a warning telling the user this.|
|Topics are referenced multiple times in the same docset.|This is a migration issue. It should not appear when the migrations are done.|
|The Ready to Publish Stage/Live flag has not been set.|These flags are mandatory and the topic cannot be published without them set.|
|Topics are not retired because they are not published to stage/live.|If the topic has not been published to stage or live, you cannot retire it. You can simply delete it then.|
|Topic has not changed since the last time it was published to stage/live.|The topic has not changed. So publishing is skipped.|

## See Also
[Finding topics with publishing errors or warnings](../Topic/Finding-topics-with-publishing-errors-or-warnings.md)

