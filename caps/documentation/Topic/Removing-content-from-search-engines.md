---
title: Removing content from search engines
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.assetid: 96088a5a-9d41-4a51-b9d9-21bdcc6e4d8c
robots: noindex,nofollow
---
# Removing content from search engines
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        
    <para>MTPS has introduced a change on their side where now the Index and Follow attributes are ignored and all the content is set to True automatically. For content published in either MSDN or TechNet that needs to be hidden from search engines, content owners need to send an e-mail to <legacyItalic>MSDNHelp</legacyItalic> with the following format. MTPS team will review the request and, if approved, will remove those topics from search engines.
</para><table>
<thead>
<tr>
<TD></TD><TD><para>Short ID</para></TD>
<TD><para>Product Family and Version</para></TD><TD><para>Locale</para></TD><TD><para>Robot Value</para></TD><TD><para>Requested By</para></TD>
</tr>
</thead>
<tbody>
<tr>
<TD><para><ui>Example</ui></para></TD><TD><para>dn720557</para></TD>
<TD><para>VS.111</para></TD><TD><para>en-us, de-de, ja-jp</para><para>(provide all locales that are being retired)</para></TD><TD><para>NoIndex/NoFollow</para></TD><TD><para>anneta</para></TD>
</tr>

</tbody>
</table></introduction>
    
    <section>
<title>Getting  the short ID, product family and Product Family version of the topic </title><content><para><mediaLinkInline>
<image xlink:href="aa9d3849-58ad-4d69-b217-101e57fa78aa"/>
</mediaLinkInline></para><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLinkInline></para></TD>
<TD><para>Go to <ui>Retired contents</ui></para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLinkInline></para></TD>
<TD><para>Click on the topic</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLinkInline></para></TD>
<TD><para>Right-click on the link next to <ui>Topic in staging</ui> label</para></TD>
</tr><tr><TD><para><mediaLinkInline>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLinkInline></para></TD><TD><para>Get the Product Family and its version from the URL</para></TD></tr>
</tbody>
</table></content>
</section><relatedTopics/>
</developerConceptualDocument>
