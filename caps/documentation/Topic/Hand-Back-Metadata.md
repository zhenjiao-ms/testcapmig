---
title: Hand Back Metadata
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2f130df-1557-4687-8221-fcd4b43aee44
---
# Hand Back Metadata
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        
    </introduction>
    <section>
                
                <content>
                    <para>For a description of the query operator values, see <link xlink:href="e28b8907-b01d-4a80-a827-008de6998049">Quick/Full-text search</link>.</para><table border="1"><tbody><tr><TD><para><ui>Hand Back Metadata Value</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD><para><ui>Query operator</ui></para></TD><TD><para><ui>In query column picker?</ui></para></TD></tr><tr><TD><para>End Date</para></TD><TD><para>Date when the hand back completed</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Failed Total</para></TD><TD><para>Total failed count of entities in the hand back</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>GUID</para></TD><TD><para>Unique identifier  of the hand back. </para></TD><TD><para>=</para><para>&lt;&gt;</para><para><ui>Under is a bug and will be removed in Phase 4</ui></para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Hand back Job Status</para></TD><TD><para>Status of the hand back</para><list class="bullet">
<listItem>
<para>Succeeded: the hand back finished successfully.</para>
</listItem>
<listItem>
<para>SucceededWithWarning: the hand back finished successfully with some warning. e.g. some XLIFF files in hand back package have invalid schema.</para>
</listItem><listItem><para>Failed: the hand back failed.</para></listItem><listItem><para>Cancelled</para></listItem><listItem><para>Paused</para></listItem><listItem><para>Pending</para></listItem><listItem><para>Processing</para></listItem>
</list></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Item Total</para></TD><TD><para>Total number  of entities included in the hand back.</para><para></para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Metadata Modified By</para></TD><TD><para>User who made latest metadata modification of the hand back</para></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Metadata Modified Date</para></TD><TD><para>Date time of the latest metadata modification</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Name</para></TD><TD><para>Name of the hand back</para></TD><TD><para>Contains</para><para>=</para><para>&lt;&gt;</para><para>Does Not Contain</para><para>Begins With</para><para>Wildcard</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Start Date</para></TD><TD><para>Date when the hand back started</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Success Total</para></TD><TD><para>Total number of succeeded entities included in the hand back</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Triggered By</para></TD><TD><para>User  who created the hand back</para></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr></tbody></table>
                </content>
            </section>
    <relatedTopics/>
</developerConceptualDocument>
