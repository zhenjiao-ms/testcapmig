---
title: Handoff Metadata
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d91a0ed-65b7-47d3-87e8-7006bfab9dad
---
# Handoff Metadata
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        
    </introduction>
    <section>
                
                <content>
                    <para>For a description of the query operator values, see <link xlink:href="e28b8907-b01d-4a80-a827-008de6998049">Quick/Full-text search</link>.</para><table border="1"><tbody><tr><TD><para><ui>Handoff Metadata Value</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD><para><ui>Query operator</ui></para></TD><TD><para><ui>In query column picker?</ui></para></TD></tr><tr><TD><para>End Date</para></TD><TD><para>Date when the handoff completed</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Failed Total</para></TD><TD><para>Amount of  entities that failed in the handoff</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>GUID</para></TD><TD><para>Unique identifier of handoff</para></TD><TD><para>=</para><para>&lt;&gt;</para><para><ui>Under is a bug and will be removed in Phase 4</ui></para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Handoff Job Status</para></TD><TD><para>Status of the handoff.</para><list class="ordered">
<listItem>
<para>Succeeded : the handoff finished successfully. </para>
</listItem>
<listItem>
<para>SuceededWithWarning : the handoff finished successfully with some warning. e.g. some of entities did  not meet handoff criteria; some entities failed. <ui>What does this mean?</ui></para>
</listItem><listItem><para>Failed : the handoff failed. <ui>What does this mean?</ui></para></listItem><listItem><para>Cancelled</para></listItem><listItem><para>Paused</para></listItem><listItem><para>Pending</para></listItem><listItem><para>Processing</para></listItem>
</list></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Item Total</para></TD><TD><para>Amount of entities included in the handoff</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Metadata Modified By</para></TD><TD><para>User who modified the metadata of the handoff</para></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Metadata Modified Date</para></TD><TD><para>Date of the latest metadata modification</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Name</para></TD><TD><para>Name of the handoff</para></TD><TD><para>Contains</para><para>=</para><para>&lt;&gt;</para><para>Does Not Contain</para><para>Begins With</para><para>Wildcard</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Start Date</para></TD><TD><para>Start date of the handoff</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Success Total</para></TD><TD><para>Total succeeded count of entities in the handoff</para></TD><TD><para>=</para><para>&gt;=</para><para>&gt;</para><para>&lt;=</para><para>&lt;</para></TD><TD><para>Yes</para></TD></tr><tr><TD><para>Triggered By</para></TD><TD><para>User who triggered this handoff</para></TD><TD><para>=</para><para>&lt;&gt;</para></TD><TD><para>Yes</para></TD></tr></tbody></table>
                </content>
            </section>
    <relatedTopics/>
</developerConceptualDocument>
