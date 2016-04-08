---
title: _retired - Publishing content in a TOC outline
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.assetid: 2b556103-5c8a-4935-9cc9-8f1bb0509043
---
# _retired - Publishing content in a TOC outline
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        <para>This topic contains the information you need to know to publish content in the TOC.  </para>
    </introduction>
    <section>
<title>Publishing the contents of the TOC</title><content><mediaLink>
<image xlink:href="71cc27b6-4c35-41d4-ad43-9c2f24ed3dc3"/>
</mediaLink><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLinkInline></para></TD>
<TD><para>Click <ui>Outline</ui> in the left-hand pane.</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLinkInline></para></TD>
<TD><para>Click on the outline you would like to publish</para></TD>
</tr><tr>
<TD><para><mediaLinkInline>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLinkInline></para></TD>
<TD><list class="bullet">
<listItem>
<para>To publish the full TOC, select the top parent topic of the outline. Make sure that no other nodes are selected.
Both checkbox and mouse focus should be in the topic.</para>
</listItem><listItem><para>To publish a topic, select the topic to publish. Make sure that the checkbox and the focus are on the topic you would like to publish. </para></listItem>
<listItem>
<para>To publish only a subset of topics, select one or multiple topics. Note that if one of the topics is a parent topic and all its children will get published. Make sure that the outline parent topic is not selected (uncheck the check box if that is active).</para>
</listItem>
</list></TD>
</tr><tr><TD><mediaLink>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLink></TD><TD><para>Click on <ui>Publishing</ui>.</para></TD></tr>

</tbody>
</table><para><mediaLinkInline>
<image xlink:href="4566567a-7a32-4659-9843-c07bfdf24407"/>
</mediaLinkInline></para><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="2d2cc7a6-19c5-42ef-af9e-f0f4b3680474"/>
</mediaLinkInline></para></TD>
<TD><para>Check your options are correct. For more information, see <link xlink:href="88d647d7-01e4-4059-bb85-7044d6a799b0">Configuring a TOC outline for publishing</link>.</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5f758df0-6bc5-4f62-92f9-7af03764a447"/>
</mediaLinkInline></para></TD>
<TD><para>Click on <ui>Publish</ui>.</para></TD>
</tr>

</tbody>
</table></content><content><para>Under <ui>Content</ui></para><list class="bullet">
<listItem>
<para>Select <ui>Topics</ui> to publish only the topics and not the full TOC. Note that if you publish a new topic or a topic that was previously published in another section of the TOC, the TOC information will also be published for that topic, so it shows in the right place in the TOC. Thus, you do not need to publish the parent topic. Note that this does not include topics underneath the TOC root node.</para>
</listItem>
<listItem>
<para>Select <ui>Outline</ui> if you have made a series of changes to the TOC and your topics have not changed. This option is only available when you select the TOC parent node.</para>
</listItem><listItem><para>Select <ui>Outline and topics</ui> if both content and TOC have changed to ensure your topics updates get published and the topics appear in the right places. This option is only available when you select the TOC parent node.</para></listItem>
</list><para>Under <ui>Publish to</ui></para><list class="bullet">
<listItem>
<para>Select <ui>Staging</ui> to publish the content to Stage. Note that the <ui>Ready to Stage</ui> attribute should be set to True. Otherwise, publishing will fail. This attribute's value will not change after publishing to stage.</para>
</listItem>
<listItem>
<para>Select <ui>Live</ui> to publish the content to Live. Note that the <ui>Ready to Publish Live</ui> attribute should be set to True. Otherwise, publishing will fail. This attribute's value will be reset to <ui>False</ui> after publishing live, to prevent content to go live by accident.</para>
</listItem>
</list><para>In CAPS, there is different flags for publishing content to stage and live. These two are independent, although you always have to publish the content to stage before it can go live.</para><para>Under <ui>Publish mode</ui></para><list class="bullet">
<listItem>
<para>By default, CAPS publishes the content in incremental mode (only the content that has changed will be sent for publishing). However, there are times that the published topic does not get published even it has changed. This is when <ui>Publish all changed and unchanged topics</ui> becomes handy. This forces publishing all the topics that are selected, regardless they have changed or not.</para>
</listItem>

</list><para>Under <ui>Locales</ui>, select</para><list class="bullet">
<listItem>
<para><ui>en-us</ui> for English content.</para>
 </listItem><listItem><para>Non <ui>en-US</ui> for localized content. Then, type or select the locales to publish.</para></listItem>

</list><para>Click on <ui>Publish</ui>.</para></content><content><para>CAPS show a publishing status. </para><para><mediaLinkInline>
<image xlink:href="ed02beb2-1998-4a05-b46c-d6de0de41d54"/>
</mediaLinkInline></para><table>
<tbody><tr>
<TD><mediaLink>
<image xlink:href="1cc8bac3-82cb-4927-ba1c-0c1095a3aedb"/>
</mediaLink></TD>
<TD><para>Once the content is published, you will see Succeeded, Published with Warnings, or Failed.</para></TD>
</tr>
<tr>
<TD><mediaLink>
<image xlink:href="f49f6ef0-9764-4006-bec1-c17bfd47835d"/>
</mediaLink></TD>
<TD><para>Click on <ui>View Details</ui> to see more details and download the publishing log to troubleshoot the error. </para></TD>
</tr>

</tbody>
</table></content><content><mediaLink>
<image xlink:href="93f53238-1df1-4bd2-9a45-f21b302d51df"/>
</mediaLink><table>
<tbody><tr>
<TD><mediaLink>
<image xlink:href="57b27918-71e0-49a8-9d8f-a9e32814649c"/>
</mediaLink></TD>
<TD><para>If publishing is successful, you can click on the version next to either Outline in staging or Outline in live to see the TOC on the stage or live environment.</para></TD>
</tr>


</tbody>
</table></content>
</section>
    <relatedTopics/>
</developerConceptualDocument>
