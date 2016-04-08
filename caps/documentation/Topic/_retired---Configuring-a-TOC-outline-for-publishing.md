---
title: _retired - Configuring a TOC outline for publishing
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.assetid: 88d647d7-01e4-4059-bb85-7044d6a799b0
---
# _retired - Configuring a TOC outline for publishing
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
    <introduction>
        <para>Before publishing, there are some attributes that you would need to select.</para>
    </introduction>
    <section>
        
        <content>
            <list class="ordered">
<listItem>
<para>Click on the outline.</para>
</listItem>
<listItem>
<para>Click on <ui>Publishing</ui>.</para>
</listItem><listItem><para>Configure the attributes you need to publish. Note the mandatory attributes.</para><table>
<thead>
<tr>
<TD><para>Attribute</para></TD>
<TD><para>Description</para></TD><TD><para>Type</para></TD><TD><para>DxStudio attribute name</para></TD>
</tr>
</thead>
<tbody>
<tr>
<TD><para>Product Family</para></TD>
<TD><para>Indicates the Product Family name getting published to MTPS. This is part of the Content Item key in MTPS that uniquely identifies content.</para></TD><TD><para>Required</para></TD><TD><para>zzpub_MtpsProductFamily</para></TD>
</tr>
<tr>
<TD><para>Product Family Version</para></TD>
<TD><para>Indicates the Product Family version getting published to MTPS. This is part of the Key that identifies a unique content item in MTPS.</para></TD><TD><para>Required</para></TD><TD><para>zzpub_MtpsVersion</para></TD>
</tr><tr><TD><para>Ready to Stage</para></TD><TD><para>Indicates that the content is ready to go to stage.</para></TD><TD><para>Required for publishing to stage</para></TD><TD><para><?xm-replace_text Type new maml:para here ?></para></TD></tr><tr><TD><para>Ready to Publish Live</para></TD><TD><para>Indicates that the content is ready to go to live.</para></TD><TD><para>Required for publishing to live</para></TD><TD><para><?xm-replace_text Type new maml:para here ?></para></TD></tr><tr><TD><para>Preferred Site</para></TD><TD><para>Indicates the canonical URL for the topics. Content will default to the MSDN site unless specified otherwise.</para></TD><TD><para>Required</para></TD><TD><para>PreferredSiteName</para></TD></tr><tr><TD><para>No Index</para></TD><TD><para>Indicates whether the topic is indexed by a search engine. False means that the topic is set for indexing.</para></TD><TD><para>Optional</para></TD><TD><para>Robots</para></TD></tr><tr><TD><para>No Follow</para></TD><TD><para>Indicates whether a hyperlink from this topic influences the link target's ranking in the search engine's index. False means that the topic will influence in the ranking.</para></TD><TD><para>Optional</para></TD><TD><para>Robots</para></TD></tr><tr><TD><para>Community Content</para></TD><TD><para>Indicates whether the Community Content pane (content wiki) appears for this article.</para></TD><TD><para>Optional</para></TD><TD><para>CommunityContent</para></TD></tr><tr><TD><para>Preferred Library</para></TD><TD><para>Indicates the canonical URL for the topics. Users can specify any value, so this is a free-text field. MTPS saves them as-is. It may or may not match the "chrome" (iroot).  For example, "windowsazure" scoped library  is a redirect handled during rendering and it has nothing to do with this field.</para></TD><TD><para>Optional</para></TD><TD><para>PreferredLib</para></TD></tr>
</tbody>
</table><alert class="note">
<para>You might have noticed that there is not <ui>MTPSTeamName</ui> attribute to set up. This is because this attribute is hidden from the user and set at the tenant level, as there is no longer need for the attribute but still is mandatory for publishing into MTPS.</para>
</alert></listItem><listItem><para>Click on <ui>Save</ui> when you are done.</para></listItem>
</list>
        <alert class="important">
<para>Make sure you click on <ui>Save</ui> before you click the <ui>Publish</ui> button. Otherwise, your unsaved changes will not be taken into account for the publishing job.</para>
</alert></content><content></content>
        
    </section>
    <relatedTopics/>
</developerConceptualDocument>
