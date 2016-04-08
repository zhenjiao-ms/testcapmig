---
title: CAPS frequently asked questions (FAQ)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfd038e0-e329-409f-9757-c43a7b0c06e7
author: Lizap
---
# CAPS frequently asked questions (FAQ)
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        <para>Here are some of the most frequently asked questions about CAPS, along with answers.</para><para>Have a new question and answer? Feel free to edit and add below.</para>
    </introduction>
    <section><title>Who can access CAPS?</title><content><para>CAPS can only be accessed with a Microsoft corpnet account.</para></content>
</section><section>
<title>Where I can access CAPS from?</title><content><para>You can access CAPS from anywhere. You do no need to be connected to corpnet, VPN, or RASS to access CAPS. Just your Microsoft corpnet credentials.</para></content>
        <sections>
        </sections>
    </section>
    <section>
<title>How do I jump to a GUID (like Ctrl+G in Dx)?</title><content><para>Just type the GUID in the Search box next to the Settings. See <link xlink:href="e28b8907-b01d-4a80-a827-008de6998049#SearchTopicGUID">Search by topic GUID</link></para></content>
</section><section>
<title>Can I publish a topic to both TechNet and MSDN?</title><content><para>CAPS doesn't actually change anything about the publishing backend - we still use the MTPS build system. So if it used to work in Dx, then it should still work in Dx.  You will need to hook up the HxT for both MSDN and TechNet for that to happen.</para></content>
</section><section>
<title>Wait, I upgraded to XMetal 9, but where is my license??</title><content><para>Tricky tricky, right? The license you used for a previous version of XMetal is no good, but you don't have to download a new one. Instead, when XMetal asks you to activate your license, navigate to the folder where you installed XMetal 9. There's a license file there - use it.</para></content>
</section><section>
<title>What browser should I be using?</title><content><para>CAPS runs in Edge, Internet Explorer, and Chrome, and we support all.</para><para>That being said, you might see better performance either in an InPrivate session of IE or by using Chrome or Edge.</para></content>
</section><section><title>How to interpret CAPS content version numbers?</title><content><para>The major/minor number for en-US content stands for ContentRevision.LocalizableMetadataRevision. Localizable metadata is those metadata that can be localized. For a topic, they include topic title, toc title, visible index keywords. If you change any one of these localizable metadata, the current minor number would increase by 1. If you change the content and check in your changes, the current major number would increase by 1.</para><para>The '*' is a indication that the there is some warning generated in the publish action.</para></content></section>
<relatedTopics/></developerConceptualDocument>
