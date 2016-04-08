---
title: Editing a topic in XMetaL
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ff7b7629-040d-435d-9f54-47425c567c92
---
# Editing a topic in XMetaL
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        <para>You need to have XMetaL and the add-in installed before you choose this option. See <link xlink:href="0c5502e1-5a1f-4613-b30e-391aade2e606">Installing XMetaL</link>.</para><para><ui>In this topic</ui></para><list class="bullet">
<listItem><para><link xlink:href="#openingtopicXMetal">Opening a topic in XMetaL</link></para></listItem><listItem><para><link xlink:href="#InsertingElements">Inserting elements quickly</link></para></listItem><listItem>
<para><link xlink:href="#InsertingImage">Inserting an image</link></para>
</listItem><listItem>
<para><link xlink:href="#InsertingToken">Inserting a token</link></para>
</listItem>

<listItem>
<para><link xlink:href="#LinkToTopic">Inserting a link to another topic (internal link)</link></para>
</listItem><listItem><para><link xlink:href="#CreatingBookmark">Adding a bookmark</link></para></listItem>

<listItem>
<para><link xlink:href="#InternalBookmark">Inserting a link to a bookmark within current topic</link></para>
</listItem><listItem><para><link xlink:href="#legacylink">Inserting a link to another topic - with custom link text</link></para></listItem><listItem>
<para><link xlink:href="#ExternalLink">Inserting a link to an external page</link></para>
</listItem><listItem><para><link xlink:href="#ExternalBookmark">Inserting a link to a bookmark to another page</link></para></listItem><listItem><para><link xlink:href="#SharedFolderLink">Inserting a link to a shared folder</link></para></listItem><listItem><para><link xlink:href="#InsertingCommonText">Inserting common text</link></para></listItem><listItem><para><link xlink:href="#workingwithtables">Working with tables</link></para></listItem><listItem><para><link xlink:href="#TrackingChanges">Tracking changes</link></para></listItem><listItem><para><link xlink:href="#workingwithcomments">Working with comments</link></para></listItem><listItem><para><link xlink:href="#ExpandedCollapsedSections">Expanded or collapsed sections</link></para></listItem><listItem><para><link xlink:href="#PreviewingTopicXMetaL">Previewing a topic </link></para></listItem><listItem>
<para><link xlink:href="#CheckingIntopic">Checking-in a topic</link></para>
</listItem>
</list>
    </introduction>
    <section address="openingtopicXMetal" DoNotNumber="true">
        
        <title>Opening a topic in XMetaL</title><content><mediaLink>
<image xlink:href="dc9b9718-a4fa-4b7f-9ce0-4e98b68859e0"/>
</mediaLink><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLinkInline></para></TD>
<TD><para>In CAPS client, highlight the topic or topics that you want to edit and use the <ui>Edit</ui> tab to choose an editor. Note that you can only open 10 topics at once in XMetaL.</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLinkInline></para></TD>
<TD><para>Use the <ui>Web</ui> editor for quick changes, like correcting a typo</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLinkInline></para></TD>
<TD><para>Use the <ui>XMetaL</ui> editor when you need to make major changes to a DDUEML topic.</para></TD>
</tr>
</tbody>
</table></content><content><mediaLink>
<image xlink:href="032f38bb-779a-44d3-bb8c-d75f5c1b2755"/>
</mediaLink></content><content><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLinkInline></para></TD>
<TD><para>Click on the CAPS toolbar icon <ui>Check Out Current Topic</ui> or press "Ctrl + Alt + O" to make the topic editable.</para></TD>
</tr>


</tbody>
</table></content>
        
    </section><section address="InsertingElements">
<title>Inserting elements quickly</title><content><para>You can insert a DDUEML element quickly in your document.</para></content><content><para><mediaLinkInline>
<image xlink:href="4000834b-bf14-44bb-9075-330d7edd83bf"/>
</mediaLinkInline></para></content><content><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLinkInline></para></TD>
<TD><para>Click on the CAPS toolbar icon <ui>Quick Insert</ui> icon or press "Ctrl + Alt + O" to bring the Quick Insert dialog.</para></TD>
</tr>


</tbody>
</table></content><content><mediaLink>
<image xlink:href="363d250c-4b99-44d8-83b5-c16cd3f3e4b7"/>
</mediaLink><table>
<tbody><tr>

<TD><para><mediaLinkInline>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLinkInline></para></TD><TD><para>Start typing the name of the element that you would like to see. A list of available elements matching your partial type will display.</para><para>Press ENTER to add the element to your topic</para></TD>
</tr>


</tbody>
</table><para><?xm-replace_text Type new maml:para here ?></para></content>
</section><section address="InsertingImage">
<title>Inserting an image</title><content><para>Before you can insert an image into your topic, you need to add the image into CAPS. See <link xlink:href="a0527748-bdad-4e6b-bafa-e04b8ddd5f73">Adding, Updating, and Managing Images</link>.</para></content><content><para><mediaLinkInline>
<image xlink:href="f1f69489-09a8-4f43-85c1-e1b1e2e3a8d6"/>
</mediaLinkInline></para></content><content><table>
<tbody><tr>
<TD><para><mediaLinkInline>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLinkInline></para></TD>
<TD><para>In the CAPS add-in tool, click on the <ui>Insert Image</ui> icon or press "Ctrl + Alt + A".
If it is disabled, it might be that you cannot insert an image in that area of the document.</para></TD>
</tr>


</tbody>
</table></content><content><para><mediaLinkInline>
<image xlink:href="8152d40c-29d1-40e2-8592-5da0520a9acc"/>
</mediaLinkInline></para><table>
<tbody>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLinkInline></para></TD>
<TD><para>Search for the image by entering the partial or complete name of the image.  You can search by the full name, partial search, or search with wildcards. Partial search finds images matching the full word, whereas wildcards "*" allows you to look for images that partially matches a word in the image name. </para><para>For example,  search for * to get all images or "XMetaL* to get all images that start with "XMetaL".</para></TD>
</tr>
<tr>
<TD><para><mediaLinkInline>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLinkInline></para></TD>
<TD><para>Click on <ui>Search</ui>.</para></TD>
</tr><tr><TD><para><mediaLinkInline>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLinkInline></para></TD><TD><para>Select the image you would like to insert (you can see a preview on the bottom left), and click on <ui>Insert</ui>.
</para></TD></tr>
</tbody>
</table></content>
</section><section address="InsertingToken">
<title>Inserting a token</title><content><para>Before you can insert a token into your topic, you need to add the image into CAPS. See <link xlink:href="e3a8c645-eb75-4926-ac07-43ba3c1827a1">Creating, Updating, and Managing Tokens</link>.</para></content><content><list class="ordered">
<listItem>
<para> Place the cursor in an area where you can insert a token.</para>
</listItem>
<listItem>
<para>In the CAPS add-in tool, click on the<ui> Insert Token</ui> icon or type "Ctrl + Alt + T".</para>
</listItem>
<listItem><para>Click on <ui>Search</ui>.</para></listItem><listItem><para>Search for the token by entering the name of the token. You can search by the full name, partial search, or search with wildcards. Partial search finds tokens matching the full word, whereas wildcards "*" allows you to look for tokens that partially matches a word in the token name. For example,  search for * to get all tokens or e* to get all tokens that start with "e".</para></listItem><listItem><para>Select the token you would like to insert (you can see the token text on the window), and click on <ui>Insert</ui>.
</para></listItem></list></content>
</section><section address="LinkToTopic">
<title>Inserting a link to another topic (internal link)</title><content><para>Before you can insert a link to another topic, that topic must exist in CAPS. See <link xlink:href="66c34def-9662-4075-acf7-bcdc212406e7">Creating, Updating, and Managing Topics</link>.</para><list class="ordered">
<listItem>
<para> Place the cursor in an area where you can insert a link.</para>
</listItem>
<listItem>
<para>In the CAPS add-in tool, click on the<ui> Insert Link</ui> icon.</para>
</listItem>
<listItem><para>Select the <ui>Topics</ui> tab.</para></listItem><listItem><para>Search for the partial or full topic title.</para></listItem><listItem><para>Click on <ui>Search</ui>.</para></listItem><listItem><para>Select the topic you would like to insert, and click on <ui>Insert</ui>.
</para></listItem></list></content>
        
        
    
</section><section address="CreatingBookmark">
<title>Adding a bookmark</title><content><para>To create a bookmark to a section within a topic, place the cursor between  the <ui>section</ui> and the  <ui>title</ui> tags, or select the <ui>title</ui> section.  Add a value to the <ui>address</ui> attribute:</para><mediaLink>
<image xlink:href="599e32c5-5e9e-4fc4-92ec-8c1014a620e9"/>
</mediaLink></content><content><para>Note that bookmarks cannot contain dashes, spaces, and have to be unique within a topic.</para></content></section><section address="InternalBookmark"><title>Inserting a link to a bookmark within current topic</title><content><para>To add a link to a bookmark:</para><list class="ordered"><listItem><para>Place the cursor in an area where you can insert a link.</para></listItem><listItem><para>Select the <ui>Insert Link</ui> icon.</para></listItem><listItem><para> Select the <ui>Bookmarks In This Topic </ui> tab.</para></listItem><listItem><para>Search for the bookmark</para></listItem><listItem><para>Select the bookmark.</para></listItem><listItem><para>Click <ui>Insert</ui>.</para></listItem></list></content>
</section><section address="legacylink">
<title>Inserting a link to another topic - with custom link text</title><content><para>You can use a &lt;legacylink&gt; tag to create a link with custom link text (instead of the default topic title).</para><list class="ordered"><listItem><para>First, you'll need the GUID of the topic you want to link to. So get that. </para><para>You can get the GUID from the <ui>General</ui> tab in CAPS, or you can insert an internal link to the topic and copy the GUID out of the <ui>xlink:href</ui> field (on the &lt;link&gt; tag). Just remember to delete the internal link, or else you'll have two links.</para></listItem><listItem><para>Now, put your cursor where you want to insert your link, and then insert the &lt;legacylink&gt; from the Element list.</para></listItem><listItem><para>Type the link text you want inside the tag.</para></listItem><listItem><para>In the Attribute Inspector, enter the GUID for the topic you want to link to in the <ui>address</ui> field..</para></listItem></list></content>
</section><section address="ExternalLink">
        <title>Inserting a link to an external page</title>
        <content>
            <list class="ordered">
<listItem>
<para> Place the cursor in an area where you can insert a link.</para>
</listItem>
<listItem>
<para>In the CAPS add-in tool, click on the<ui> Insert Link</ui> icon.</para>
</listItem>
<listItem><para>Click on the <ui>External links</ui> tab.</para><alert class="tip">
<para>If you would like the Link URL and the Text to display to match, select <ui>Match to URL</ui>.</para>
</alert></listItem><listItem><para>Enter the URL in the <ui>Link URL</ui> text box.</para></listItem><listItem><para>Enter the text for the link in the <ui>Text to Display</ui> text box.
</para></listItem></list>
        </content>
        
    </section><section address="ExternalBookmark">
<title>Inserting a link to a bookmark in  another topic</title><content>
            <list class="ordered">
<listItem>
<para> Place the cursor in an area where you can insert a link.</para>
</listItem>
<listItem>
<para>In the CAPS add-in tool, click on the<ui> Insert Link</ui> icon.</para>
</listItem>
<listItem><para>Select the <ui>Topics</ui> tab.</para></listItem><listItem><para>Search for the partial or full topic title.</para></listItem><listItem><para>Click on <ui>Search</ui>.</para></listItem><listItem><para>Click on the topic.</para></listItem><listItem><para>Click on <ui>Show  Bookmarks</ui> button. Another list view shows up below the topic list view.</para></listItem><listItem><para>	Click a bookmark in the list.</para></listItem><listItem><para>lick <ui>Insert</ui> to insert the bookmark and close the current window.</para></listItem></list>
        </content>
</section><section address="SharedFolderLink">
<title>Inserting a link to a shared folder</title><content><para>You can insert a link to a shared folder in your documentation by  using  an external link and typing in the address field <legacyItalic>file:///&lt;path&gt;. Example: file:///\\uafsall02\Public\XMetaL9</legacyItalic>. This might become handy to we may want to point TAP/NDA customers to an internal shared folder from the docs in future private release documentation.</para></content>
</section><section address="InsertingEmailAddress">
<title>Inserting e-mail addresses</title><content><para>You can insert a link to an e-mail address  in your documentation by  using  an external link and typing in the address field <legacyItalic>mailto:&lt;email-address&gt;. Example: mailto:saldana@microsoft.com</legacyItalic>.</para></content>
</section><section address="InsertingCommonText">
<title>Inserting common text</title><content><para>The <ui>Insert Common Text</ui> tool allows you to insert commonly used XML structures into your topic. For example, you can insert a table and then add or delete rows and columns and enter text as needed. </para></content>
<sections>
            <section>
                
                <content>
            <list class="ordered">
<listItem>
<para> Place the cursor in an area where you can insert common text.</para>
</listItem>
<listItem>
<para>In the CAPS add-in tool, click on the <ui> Insert Common Text</ui> icon <mediaLinkInline>
<image xlink:href="2e02f20f-38a2-4d74-af6b-928883482e18"/>
</mediaLinkInline>.</para>
<alert class="note">
<para>If you try to insert a Common Text element in a location not allowed by the schema, XMetaL will issue you the following warning:<br/><mediaLinkInline>
<image xlink:href="8ce360b8-70ba-4c27-8fef-f1d11fc793b1"/>
</mediaLinkInline></para>
</alert></listItem>
<listItem><para>Select the desired XML structure name from the <ui>Common text </ui>drop-down list; see the list of default entries below.
</para></listItem><listItem><para>Click on <ui>Insert</ui>.</para></listItem></list>
        </content>
            </section><section>
<title>List of Common Text Entries</title><content><list class="bullet">
<listItem>
<para><ui>Alert - Caution</ui></para>
</listItem>
<listItem>
<para><ui>Alert - Important</ui></para>
</listItem><listItem><para><ui>Alert - Note</ui></para></listItem><listItem><para><ui>Alert - Tip</ui></para></listItem><listItem><para><ui>Alert - Warning</ui></para></listItem><listItem><para><ui>Code block</ui> - Inserts a code block with C# as the default language.</para></listItem><listItem><para><ui>Definition Table</ui></para></listItem><listItem><para><ui>List - Bulleted</ui> - Inserts a bulleted list with two items.</para></listItem><listItem><para><ui>List - Numbered</ui> - Inserts a numbered  list with two items.</para></listItem><listItem><para><ui>Procedure</ui> - Inserts a procedure with two steps.</para></listItem><listItem><para><ui>Table with Header</ui> - Inserts a 2-column, 2-row table with a header row as the top row</para></listItem><listItem><para><ui>Table without Header</ui> - Inserts a 2-column, 3-row table with no header row</para></listItem>
</list><alert class="important">
<para>Note that as dynamic links table are not supported in CAPS, the <ui>Dynamic Links Table</ui> is missing from this list when compared with DxStudio. All the other Common Text elements are the same than DxStudio</para>
</alert><alert class="important">
<para>You cannot create additional entries for common text at this point.<br/>A common text insertion can be undone via a single Undo or CTRL+Z</para>
</alert></content>
</section>
        </sections></section><section address="workingwithtables">
<title>Working with tables</title><content><para>Working with tables in XMetaL is still difficult. However, you can get a lot of help if you use the XMetaL toolbar once you have inserted a table as explained in the <link xlink:href="#InsertingCommonText">Inserting common text</link>section.</para><para>Please note that XMetaL has the following limitations and there is not much the CAPS team can do about it without having to recreate the table functionality:</para><list class="bullet">
<listItem>
<para>You cannot delete multiple table rows in a single operation. You can do only one row at a time. </para>
</listItem><listItem><para>If you insert a new row or cell, this one will not have the <legacyItalic>&lt;para&gt;</legacyItalic> elements inserted. In order to insert one, you need to insert the <legacyItalic>&lt;para&gt;</legacyItalic> element or start typing into the cell.</para></listItem>
<listItem>
<para>You cannot paste text into a table cell if the cell does not contain the &lt;para&gt; element already. 
</para>
</listItem>
</list></content>
</section><section address="TrackingChanges">
<title>Tracking changes</title><content><list class="ordered"><listItem><para>In XMetal, go to <ui>View</ui> - <ui>Toolbars</ui>, and confirm that the <ui>Reviewing</ui> toolbar is selected.</para></listItem><listItem><para>Use the following icons on Reviewing toolbar to track changes.</para></listItem></list><mediaLink>
<image xlink:href="21e9b368-9d25-4aec-b5fd-340303790a03"/>
</mediaLink><table border="1"><tbody><tr><TD><mediaLink>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLink></TD><TD><para>Click to turn track changes on and off.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLink></TD><TD><para>Click to navigate to the previous change.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLink></TD><TD><para>Click to navigate to the next change.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLink></TD><TD><para>Click to accept the selected change.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="2d2cc7a6-19c5-42ef-af9e-f0f4b3680474"/>
</mediaLink></TD><TD><para>Click to reject the selected change.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5f758df0-6bc5-4f62-92f9-7af03764a447"/>
</mediaLink></TD><TD><para>Click to accept all changes, reject all changes, and navigate to changes.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="2fcfbefc-61d5-404d-9591-6983d464458c"/>
</mediaLink></TD><TD><para>Click to configure the formatting of inserted and deleted text.</para></TD></tr></tbody></table></content>
</section><section address="workingwithcomments">
<title>Working with comments</title><content><list class="ordered"><listItem><para>In XMetal, go to <ui>View</ui> - <ui>Toolbars</ui>, and confirm that the <ui>CAPS</ui> toolbar is selected.</para></listItem><listItem><para>Use the following icons on the  toolbar to manage comments.</para></listItem></list><mediaLink>
<image xlink:href="183e0bb3-5154-49c2-b57a-e4d00f172a95"/>
</mediaLink><table border="1"><tbody><tr><TD><mediaLink>
<image xlink:href="a2b4ccfd-2afb-447b-a970-d268bc43a798"/>
</mediaLink></TD><TD><para>Click to insert a comment.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5199819d-555f-46ff-8be4-ac6e2fe3af4a"/>
</mediaLink></TD><TD><para>Click to delete a selected comment.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5e6746cd-a7c7-4d9a-88cf-3ec060ed1b1f"/>
</mediaLink></TD><TD><para>Click to delete all comments.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="6a16037b-01a0-44b5-bb9c-4234cb2c0187"/>
</mediaLink></TD><TD><para>Click to navigate to the previous comment.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="2d2cc7a6-19c5-42ef-af9e-f0f4b3680474"/>
</mediaLink></TD><TD><para>Click to navigate to the next comment.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="5f758df0-6bc5-4f62-92f9-7af03764a447"/>
</mediaLink></TD><TD><para>Click to show all comments.</para></TD></tr><tr><TD><mediaLink>
<image xlink:href="2fcfbefc-61d5-404d-9591-6983d464458c"/>
</mediaLink></TD><TD><para>Click to hide all comments.</para></TD></tr></tbody></table></content>
</section><section address="ExpandedCollapsedSections">
<title>Expanded or collapsed sections</title><content><para>By default, you can choose whether a certain section in your document will be expanded or collapsed. By default, all sections are expanded, so you only need to do this if you would like to have some sections collapsed by default in the published topic.</para><list class="ordered">
<listItem>
<para>In XMetaL, place the cursor just next to the opening <ui>sections</ui> or <ui>section</ui> tag.</para>
</listItem>
<listItem>
<para>In the Attribute Inspector click on the <ui>expanded</ui> attribute. <mediaLinkInline>
<image xlink:href="32ad9278-7c66-4de5-8635-95184b29f7e9"/>
</mediaLinkInline></para>
</listItem><listItem><para>Select <ui>false</ui> to collapse the section. Setting it to <ui>true</ui> or leaving it blank will show your section expanded by default once the topic is published.</para></listItem>
</list></content></section><section address="PreviewingTopicXMetaL"><title>Previewing a topic </title><content>
            
        <list class="ordered">
<listItem>
<para>In XMetaL, go to <ui>View</ui> - <ui>Page Preview</ui>.
</para>
</listItem>
<listItem>
<para>Or click the Page Preview icon at the bottom right area in the XMetaL editor <mediaLinkInline>
<image xlink:href="9fae4184-158e-409a-ade6-87b4c08e1dc2"/>
</mediaLinkInline>.</para>
</listItem>
</list></content>
</section><section address="CheckingIntopic">
<title>Checking-in a topic</title><content>
            <list class="ordered">


<listItem><para>Once you finish your changes, click on the  <ui>Check In Current Topic</ui> icon on the CAPS toolbar.</para></listItem><listItem><para>Add a check-in comment and click <ui>OK</ui>.</para></listItem><listItem><para>The topic gets checked-in and stay open in XMetaL as read-only.</para></listItem></list>
        </content>

</section>
    <relatedTopics/>
</developerConceptualDocument>
