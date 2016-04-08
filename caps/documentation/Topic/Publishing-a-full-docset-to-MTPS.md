---
title: Publishing a full docset to MTPS
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbfb8957-60af-4bc2-a9ee-edaa8a38a642
---
# Publishing a full docset to MTPS
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        
    <para>In order to publish topics to MTPS or create offline content (such as CHM), you need to create and maintain a docset.  	 See <link xlink:href="dc59db49-77a4-4227-878a-8bf2e8ae4575">Managing docsets</link> for information about how to create a docset, include content from another docset,  include topics outside your portfolio, etc.</para></introduction>
    <section>
<content><alert class="important">
<para>You can only publish a docset at a time. </para>
</alert><alert class="tip">
<para>You could share a docset into another docset and publish them together.</para>
</alert></content>
</section><section address="PubDocset"><title>Setting the docset attributes</title><content><list class="ordered">
<listItem>
<para>Select the docset</para>
</listItem>
<listItem>
<para>Click on <ui>Publishing</ui></para>
</listItem><listItem><para>You can set different attributes at the docset level. The following is not an exhaustive list,just the mandatory attributes and those to watch out for.  For a full description of the available attributes, please see <link xlink:href="4b5037d3-e7b3-41b8-a0de-b67afdf42d92">Docset Metadata</link>. </para><alert class="tip">
<para>Note that in order to publish to MTPS, the mandatory attributes need to be set. </para>
</alert><table border="1"><thead><tr><TD><para>Attribute name</para></TD><TD><para>Optional or required for MTPS publishing</para></TD></tr></thead><tbody><tr><TD><para><ui>Product Family</ui></para><para><ui>Product Family  Version</ui></para></TD><TD><para>Required</para><alert class="tip">
<para>If you cannot find your Product Family or Product Family Version, please open a Live Site Issue.  See <link xlink:href="468cf100-8e42-47b2-9373-f61ceeb5c2f9">How to file a Live Site Issue (LSI) in TFS</link>.</para>
</alert></TD></tr><tr><TD><para>Preferred Site</para></TD><TD><para>Optional. It is recommended you set up this attribute at the docset level.</para></TD></tr><tr><TD><para>Preferred Library</para></TD><TD><para>Optional. It is recommended you set up this attribute at the docset level.</para></TD></tr><tr><TD><para><ui>DCS.</ui>xxx attributes. Please ignore these as they will be removed as they are obsolete.</para></TD><TD><para>Optional</para></TD></tr></tbody></table></listItem>
</list></content>
</section><section>
<title>Publishing the docset</title><content><alert class="important">
 <para>Make sure you read the topic <link xlink:href="bd4bd301-db92-4484-a9a6-fa2469e73133">Understanding publishing to MTPS</link> before you start publishing from CAPS. There are some differences when you publish to stage and live, as well as between content and TOC publishing you should be aware. </para>
</alert><alert class="note">
 <para>Note only the content of the topics that have the Ready to Stage flag set (if you publish to stage) or the Ready to Live flag set (if you publish to live) will be published. Also, there are some attributes that are mandatory for topic publishing. See <link xlink:href="1cfa3651-93d1-454d-8c03-685028a04adf">Publishing individual topics to MTPS</link>.</para>
</alert><list class="ordered">
<listItem>
<para>If you are ready to publish the docset, click on <ui>Publish</ui></para>
</listItem>
<listItem>
<para>Under <ui>Content</ui> select</para><list class="bullet">
<listItem>
<para><ui>DocSet</ui> - To publish all the content in <ui>TOC</ui>, <ui>Not in TOC</ui>, and <ui>Retired contents</ui> sections.</para>
 <para>For the contents in the TOC, this will publish both the topics and the TOC.</para></listItem><listItem><para><ui>TOC (Both TOC and topics)</ui> - To publish only the topics and the TOC within the <ui>TOC</ui> section (content in <ui>Not in TOC</ui> and <ui>Retired contents</ui> sections will not be published). </para></listItem><listItem><para><ui>TOC (Only TOC)</ui> - To publish only the TOC. This is useful when you have done TOC changes but the topics have not changed.</para></listItem><listItem><para><ui>TOC (Only topics)</ui> - To publish the topics only without the TOC.</para></listItem><listItem><para><ui>Retired Contents</ui> - To publish the content in the<ui> Retire contents</ui> section. See <link xlink:href="8ff7e00d-fd2a-433f-a550-c3556d2c5c87">Retiring content (AKA Paving over)</link> for more information.</para></listItem>

</list>
</listItem><listItem><para>Under<ui> Publish to</ui> select</para><list class="bullet">
<listItem>
<para><ui>Staging</ui> - To publish the docset to staging.   You always have to publish to stage before publishing live. See <link xlink:href="bd4bd301-db92-4484-a9a6-fa2469e73133">Understanding publishing to MTPS</link>.</para>
 </listItem><listItem><para><ui>Live</ui> - To publish the docset to live. </para></listItem>

</list></listItem><listItem><para> <ui> Publish all changed and unchanged topics</ui></para><list class="bullet">
<listItem>
<para><legacyItalic>Unchecked</legacyItalic> - To publish only the topics that changed since the last time that were published last.</para>
 </listItem><listItem><para><legacyItalic>Checked</legacyItalic> - To publish all the topics regardless of whether they have changed or not since they were published last. This is useful when the content is not published to MTPS even if it has changed. </para></listItem>

</list></listItem><listItem><para>Under <ui>Locales</ui> select</para><list class="bullet">
<listItem>
<para><ui>en-us</ui> - To publish English content.  </para>
 </listItem><listItem><para><ui>Non en-us</ui> - To publish localized content. Then select the locales you would like to publish.</para></listItem>

</list></listItem><listItem><para> <ui>Force ready</ui>. This is only show if you select a different locale than en-us. </para><list class="bullet">
<listItem>
<para><legacyItalic>Unchecked</legacyItalic> - To publish to stage or live only the topics that have the corresponding <ui>Ready to Stage</ui> or <ui>Ready to publish live</ui> option turned on.</para>
 </listItem><listItem><para><legacyItalic>Checked</legacyItalic> - To override the corresponding<ui> Ready to Stage</ui> or <ui>Ready to publish live</ui> flag  and publish all the topics in the docset to stage or live, depending on your preference.</para> </listItem>

</list></listItem><listItem><para>Click <ui>Publish</ui> once you are ready to publish. </para></listItem><listItem><para>You can see the publishing status in the docset <ui>Publishing</ui> panel, under <ui>Publishing Status</ui>.</para></listItem><listItem><para> Expand the  <ui>Publishing Status</ui> section and then either Stage or Live to see more details or download the publishing report. You can also go to the History tab. See <link xlink:href="927ac1bf-c6ad-4286-b7cd-5fc04c4c6444">Viewing publishing history</link>.</para></listItem>
</list><para>If publishing succeeds with warnings or if publishing fails, consider <link xlink:href="eb3a9217-9653-4cf7-870c-6b16218da32f">Finding topics with publishing errors or warnings</link>.</para></content>
</section><section address="ViewPubContent">

<title>Viewing the published content</title><content><mediaLink>
<image xlink:href="b96fb8d5-f35c-4609-9182-0929b22e4cff"/>
</mediaLink><table border="1"><tbody><tr><TD><mediaLink>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLink></TD><TD><para>Select the topic you would like to see the published version.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLink></TD><TD><para>Click on the number next to <ui>Topic in staging</ui> or <ui>Topic in  live</ui> or in the numbers on the top right in the topic preview, to see the topic either on the MSDN or TechNet Library on  stage or in live respectively.</para></TD></tr></tbody></table></content>
</section><section><title>TOC Hookup</title><content><para>You might notice that your content might not show up in the TOC. For any docset that is not share into another docset, you still need to hookup the TOC via HxT as it was done in DxStudio. Contact your Ops/Support team for guidelines about to hookup the TOC.</para></content>
</section>
    <relatedTopics/>
</developerConceptualDocument>
