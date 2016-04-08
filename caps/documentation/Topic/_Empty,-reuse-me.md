---
title: _Empty, reuse me
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4c81f2ab-80cb-42dd-8967-099f10c18964
robots: noindex,nofollow
---
# _Empty, reuse me
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        
    <para>This topic contains all the functionality supported so far in CAPS, list of adoption blockers, and what is coming in next sprints.</para><para><ui>In this topic, we list the feature status for</ui></para><list class="bullet">
<listItem><para><link xlink:href="#AdoptionBlocker">Adoption blockers</link><ui></ui></para></listItem><listItem><para><link xlink:href="#WebClient">Web client</link></para></listItem><listItem><para><link xlink:href="#Search">Search</link></para></listItem><listItem><para><link xlink:href="#DocSet">DocSets</link></para></listItem><listItem>
<para><link xlink:href="#DDUEMLAuthor">DDUEML Authoring</link></para></listItem><listItem><para><link xlink:href="#MREF">MRef</link></para>
</listItem><listItem><para><link xlink:href="#ExternalCode">External code snippets</link></para></listItem>
<listItem>
<para><link xlink:href="#LOC">Localization</link></para></listItem><listItem><para><link xlink:href="#Publishing">Publishing</link></para></listItem>
<listItem><para><link xlink:href="#MD"> Markdown</link></para></listItem><listItem><para><link xlink:href="#UserPerm">User Permission</link></para>
</listItem><listItem><para><link xlink:href="#UnavailableFeatures">Unavailable features</link></para></listItem></list></introduction>
    <section address="AdoptionBlocker">
<title>Active adoption blockers</title><content><para>The following items are issues found that will block migration for one or more teams.</para><table>
<thead>
<tr>
<TD><para>Issue number</para></TD>
<TD><para>Issue description</para></TD><TD><para>First team to migrate blocked</para></TD><TD><para>Expected resolution date</para></TD>
</tr>
</thead>
<tbody>
<tr>
<TD><para><externalLink><linkText>13575</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/13575</linkUri></externalLink></para></TD>
<TD><para>Topic and image metadata changes whenever any field changes. This makes localization metadata validation impossible.</para></TD><TD><para>SQL 14 and other teams to migrate after that have a big amount of conceptual content and images.</para></TD><TD><para>Sprint 81 (April 10)</para></TD>
</tr><tr><TD> <para><externalLink><linkText>9882</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/9882</linkUri></externalLink></para></TD><TD><para>It is not possible to do cross-topic bookmarks. This is widely used among all the teams.</para></TD><TD><para>SQL14</para></TD><TD><para>TBD. Under investigation.</para></TD></tr><tr><TD><para><externalLink><linkText>13567</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/13567</linkUri></externalLink></para></TD><TD><para>Publishing a DocSet that has one or more topics with "Ready to Stage=FALSE" gives a publishing error message. The message misleads the users, as content publishes correctly.</para></TD><TD><para>SQL14</para></TD><TD><para>Sprint 80 (March 20)</para></TD></tr><tr><TD><para><externalLink><linkText>13573</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/13573</linkUri></externalLink></para></TD><TD><para>User does not get an error message when deleting a dependency</para></TD><TD><para>SQL14</para></TD><TD><para>Sprint 81 (April 10)</para></TD></tr><tr><TD><para><externalLink><linkText>1031</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1031</linkUri></externalLink></para></TD><TD><para>We cannot find tokens by partial values</para></TD><TD><para>SQL14</para></TD><TD><para>TBD. Under investigation</para></TD></tr><tr><TD><para><externalLink><linkText>1090</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1090</linkUri></externalLink></para></TD><TD><para>Windows Server and System Center dev content relies on HxS to hook Dx content together with WDCML content for publishing. To migrate the Dx content to CAPS, they need equivalent functionality. Megan and Lee will investigate whether we can have the equivalent of external placeholder in WDCML.</para></TD><TD><para>Parts of Windows Server (Wisky)</para></TD><TD><para>Phase 4</para></TD></tr>

</tbody>
</table></content></section><section address="WebClient"><title>Web client</title><content><table border="1"><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para></para></TD><TD><para>Create, update, preview, and metadata management for topic.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Creating, Updating, and Managing Topics</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832144.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Add, update, preview, and metadata management for images</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Adding, Updating, and Managing Images</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832140.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Create, update, preview, and metadata management for tokens</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Creating, Updating, and Managing Tokens</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832149.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD><para>	History for</para><list class="bullet">
<listItem>
<para>Topic</para>
</listItem>
<listItem>
<para>Image</para>
</listItem><listItem><para>Token</para></listItem>
</list></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Creating, Updating, and Managing Topics</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832144.aspx</linkUri></externalLink></para><para><externalLink><linkText>Adding, Updating, and Managing Images</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832140.aspx</linkUri></externalLink></para><para><externalLink><linkText>Creating, Updating, and Managing Tokens</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832149.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD><para>Grouping functionality for</para><list class="bullet">
<listItem>
<para>Image</para>
</listItem>
<listItem>
<para>Token</para>
</listItem><listItem><para>Handoff</para></listItem><listItem><para>Hand back</para></listItem><listItem><para>Topics that’s not in TOC</para></listItem><listItem><para>Retired content</para></listItem><listItem><para>Team query</para></listItem>
</list></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>	Soft deletion and Restore
</para><list class="bullet">
<listItem>
<para>Topic</para>
</listItem>
<listItem>
<para>	Image</para>
</listItem><listItem><para>Token</para></listItem><listItem><para>Folder</para></listItem>
</list></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>	Display topic checked out status in CAPS client</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Control layout rearranges based on screen resolution</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Retain multi-selection across page boundaries</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Metadata grouping – required and optional</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Remember selection when moving between folders</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Spell checker for text boxes</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Show dependency for topics</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Topic dependency error in topic preview</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Notification Service</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Pagination - infinite scroll (flat view, to be retired at the completion of S80)</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Inline code snippet syntax highlighted in preview</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Duration of notifications extended from 5 sec to 15 seconds</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Cut and paste of assets into folders</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Sorting in trash folder</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>	Keep state change when switching between different folders</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>9533</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=9533</linkUri></externalLink></para></TD><TD><para>Display TOC GUID for any topic</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 might get cut</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>11112</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11112</linkUri></externalLink></para></TD><TD><para>Support for WEDCS metadata</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr></tbody></table></content><content><para>Renaming a portfolio is not available. Tracked in feature request #<externalLink><linkText>4476</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=4476</linkUri></externalLink></para></content>
</section><section address="Search"><title>Search</title>
        <content>
            <table border="1"><thead><tr><TD><para>Full-text search</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD></TD><TD><para>Scope to a certain doc set or folder to search topics with specific topic title</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD><para></para></TD></tr><tr><TD></TD><TD><para>Support sorting by relevance in search</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para></para></TD></tr><tr><TD></TD><TD><para>Highlight search keyword in the result</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Search by image name</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para></para></TD></tr><tr><TD></TD><TD><para>Search by token name</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para></para></TD></tr></tbody></table>
        <table border="1"><thead><tr><TD><para>	Advanced Search / Query</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD></TD><TD><para>	Team queries</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Default Queries for most-used queries</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Scoped queries for asset type</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Sorting by columns in the query results</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Add/remove fields in the query results</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Search token by name and token text</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Search by locale</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Query by publishing metadata</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Queries can use macro, i.e. @Me and @Today can be used</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Queries can be cut and paste to other folders</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Query children under any parent node/folder</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Grouping and sorting for topic dependency</para></TD><TD></TD><TD></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1137</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1137</linkUri></externalLink></para></TD><TD><para>Search by publishing the last errors and warnings per topic</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1035</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1035</linkUri></externalLink></para></TD><TD><para>Find topics whose dependency has change but content has not</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1116</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1116</linkUri></externalLink></para></TD><TD><para>Export the results of my query results</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>6412</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=6412</linkUri></externalLink></para></TD><TD><para>Private queries</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P3 might be cut</para></TD><TD></TD></tr></tbody></table></content>
        
    </section><section address="DocSet">
<title>DocSets</title><content><table border="1"><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD></TD><TD><para>Create a docs set</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Add topics to docs sets</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Organize the TOC by creating multi-level hierarch</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Perform single and multiple selection of topics</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Move topics within a docset</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Reference to another docset withi the portfolio</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Reference to another TOC in a different portfolio (or outside CAPS?)</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Topic preview</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>	Options to publish the selected topics, whole doc set, or TOC</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Navigation from dependencies and query result list to the doc set (topic)</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Open the first doc set automatically when opening a portfolio</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD><TD></TD></tr></tbody></table></content>
</section><section address="DDUEMLAuthor">
<title>DDUEML Authoring</title><content><table border="1"><thead><tr><TD><para>General</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para><externalLink><linkText>6493</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/6493</linkUri></externalLink></para></TD><TD><para>Reduced amount of DDUEML conceptual templates</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO, add this info. Also, add mapping for templates no longer supported.</para></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>XMetaL</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD></TD><TD><para>Support for XMetaL 9</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Verification pending.</para></TD><TD></TD></tr><tr><TD><para></para></TD><TD><para>Launch XMetaL directly for single or bulk topic editing from CAPS client</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Editing a topic in XMetaL</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>	Plugin to make common tasks easier: 

inserting links, tokens, arts; comments management, etc.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Editing a topic in XMetaL</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Auto update of plugin</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Installing XMetaL 7.0</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para>N/A. Part of XMetaL</para></TD><TD><para>Revision marks / Tracking changes</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Editing a topic in XMetaL</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Quick insert for elements</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Editing a topic in XMetaL</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Save draft to the server</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Editing a topic in XMetaL</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832139.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Topic dependency error in topic preview</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Creating, Updating, and Managing Topics</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn832144.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para><externalLink><linkText>6489</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=6489</linkUri></externalLink></para></TD><TD><para>Configuration for broken dependencies to be publishing warnings or errors</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 might get cut</para></TD><TD></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Web editor</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para></para></TD><TD><para>Web editor for raw XML for quick changes</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO page</para><para><externalLink><linkText>Editing a topic in the web editor</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936516.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Check out/check in/undo checkout</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO page</para><para><externalLink><linkText>Editing a topic in the web editor</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936516.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Save draft to the server</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO page</para><para><externalLink><linkText>Editing a topic in the web editor</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936516.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Autosaving to the server</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO page</para><para><externalLink><linkText>Editing a topic in the web editor</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936516.aspx</linkUri></externalLink></para></TD></tr></tbody></table></content>
</section><section address="MREF">
        
        <title>MRef</title><content>
               <para>Phase 2 MREF features</para><table border="1"><tbody><tr><TH><para>Reflection</para></TH><TD></TD><TD></TD><TD></TD><TD></TD></tr><tr><TD><para>Feature</para></TD><TD><para>Description</para></TD><TD></TD><TD><para>Status</para></TD><TD><para>How-to</para></TD></tr><tr><TD><para><externalLink><linkText>1419</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Reflection can be configured via the CAPS client. 
</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><link xlink:href="d855d8d5-d4e7-4d17-9a3d-12228d4c9c63">Reflection and Comment Import</link></para></TD></tr><tr><TD></TD><TD><para>Permission to reflect can be granted to anyone collaborating on mref (writers, product PMs, etc.).</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Currently available to all users. Reflection permission group to be added in Phase 3 for more granular control <externalLink><linkText>12076</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD></TD></tr><tr><TD></TD><TD><para>DLLs and dependencies can be accessed from a network share for which permissions are granted to the designated CAPS alias.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>DLLs and dependencies can be specified individually or by folder.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>DLLs and dependencies can be accessed from product build shares. </para></TD><TD><mediaLink>

<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Reflection can use multiple versions of dependency DLLs.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>9315</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Refection can be updated.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Reflection can be recurring.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1396</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Reflection can be tokenized (auto-updating).</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1353</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para><para><externalLink><linkText>1403</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Reflection can be configured with one of three aggregation options:</para><list class="bullet"><listItem><para>Overload (default): All overloads in one topic.</para></listItem><listItem><para>Type: A type and all its members in one topic.</para></listItem><listItem><para>None: Each type and member is its own topic (DxStudio parity).</para></listItem></list></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>8546</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Namespaces can optionally be grouped. This adds an intermediate TOC level to sub-group namespaces by the first two decimal places, e.g. all namespaces beginning with “System.Build” are a group.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified. May need additional configurability in a later sprint (e.g. group by three places), or may be removed, depending on demand. </para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1356</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Reflection can be configured to show syntax in one or more supported language:</para><list class="bullet"><listItem><para>C#</para></listItem><listItem><para>C++</para></listItem><listItem><para>F#</para></listItem><listItem><para>Visual Basic</para></listItem></list></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>10477</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Reflection generates a discrete mref docset that can be shared into other docsets, but cannot have docsets shared into it.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TO DO: link to docset sharing topic when ready.</para></TD></tr><tr><TD><para><externalLink><linkText>1401</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>CAPS maintains a global dependencies cache to facilitate reflection.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Implemented, with limitations (see below).</para></TD><TD><para><link xlink:href="9d9dddd3-f43b-4eb6-8ace-f8c9ae470ed5">Global Dependencies Cache</link></para></TD></tr><tr><TD><para><externalLink><linkText>1362</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para><para><externalLink><linkText>7037</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Public namespaces, types, and members in the DLL can be excluded from CAPS. Two options:</para><list class="bullet"><listItem><para>EditorBrowsable(Never) is supported, enabling product teams to exclude APIs from both IDE browsing and CAPS content.</para></listItem><listItem><para>DxStudio ripping files are supported for migration. New design: APIs referenced by reflected APIs cannot be ripped. This is to ensure complete documentation. Migrating teams may have to document some APIs that were ripped in DxStudio.</para></listItem></list></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><link xlink:href="0ae90acb-83ac-4b36-a4fb-d28285a3c72e">Excluding APIs ("Ripping")</link></para></TD></tr><tr><TD><para><externalLink><linkText>1412</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems</linkUri></externalLink></para></TD><TD><para>Same-named namespaces can be published from multiple docsets without requiring product family version hacks, by configuring one docset (e.g. the .NET Framework class library) as the “canonical” version and other docsets with the same namespace as non-canonical. Non-canonical docsets will be published by numeric ID rather than by fully-qualified name.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Verification pending.</para></TD><TD><para><link xlink:href="c3634122-d850-41b5-bdab-2ad32ed7ace7">Canonical Namespaces</link></para></TD></tr></tbody></table>
        <table border="1"><tbody><tr><TH><para>XML comments</para></TH><TD></TD><TD></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1365</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1365</linkUri></externalLink></para></TD><TD><para>XML (triple slash) comments can be imported into mref topics via the CAPS client as part of reflection.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD><para><externalLink><linkText>1378</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1378</linkUri></externalLink></para></TD><TD><para>All elements recommended by the C# Programming Guide (except &lt;includes&gt;) are supported.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD><para><externalLink><linkText>7655</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/7655</linkUri></externalLink></para></TD><TD><para>XML comment import supports &lt;see href=””&gt; for external links.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD><para><externalLink><linkText>1381</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1381</linkUri></externalLink></para><para><externalLink><linkText>6985</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=6985</linkUri></externalLink></para></TD><TD><para>XML comments can be updated with two options:
</para><list class="bullet"><listItem><para>•	CAPS wins (default): Comments that have been human-authored in CAPS will not be overwritten.</para></listItem><listItem><para>•	Overwrite all: All comments will be overwritten with XML comment content in case of conflicts.</para></listItem></list></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Implemented, with potential issue that all migrated content will be considered non-human authored.</para></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Stubbing &amp; authoring</para></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><externalLink><linkText>1388</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1388</linkUri></externalLink></para></TD><TD><para>Mref topics can be edited in XMetal</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD></TD><TD><para>Mref topics can be edited in the web browser (raw XML).</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in production.</para></TD></tr><tr><TD><para><externalLink><linkText>9781</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=9781</linkUri></externalLink></para></TD><TD><para>Thread Safety section is auto-generated with default text. User can manually add a section to override default.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Build &amp; publishing</para></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><externalLink><linkText>9317</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=9317</linkUri></externalLink></para></TD><TD><para>Mref publishing experience is consistent with conceptual (same attributes, same UI, etc.).</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD></TD><TD><para>Single-topic publishing is supported for mref docsets.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD></TD><TD><para>Mref topics can be published incrementally (only changed topics are published).</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification in new docset design.</para></TD></tr><tr><TD><para><externalLink><linkText>7074</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=7074</linkUri></externalLink></para></TD><TD><para>Mref content can be built as XML IntelliSense files (one per assembly).</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Feature in progress.</para></TD></tr><tr><TD><para><externalLink><linkText>10478</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=10478</linkUri></externalLink></para></TD><TD><para>Mref docsets can be deleted (soft delete).</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>May be cut.</para></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Localization</para></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD></TD><TD><para>Mref localization experience is consistent with conceptual.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Verification in progress.</para></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Metadata, query &amp; history</para></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><externalLink><linkText>6769</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=6769</linkUri></externalLink></para></TD><TD><para>APIScan metadata is auto-generated for mref during reflection.</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD></tr><tr><TD><para><externalLink><linkText>7777</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/7777?fullScreen=false</linkUri></externalLink></para></TD><TD><para>APIScan metadata can be manually added to unmanaged reference topics.</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>In scope, but not yet available.</para></TD></tr><tr><TD><para><externalLink><linkText>8609</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=8609</linkUri></externalLink></para></TD><TD><para>APIs can be flagged as internal only at the type or member level, including aggregated topics, and internal only boilerplate is stubbed into topics.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Pending verification.</para></TD></tr><tr><TD><para><externalLink><linkText>11395</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/11395?fullScreen=false</linkUri></externalLink></para></TD><TD><para>Reflection recognizes IsObsolete attribute in DLLs and stubs deprecation boilerplate in topics.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Verification in progress.</para></TD></tr><tr><TD><para><externalLink><linkText>9316</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=9316</linkUri></externalLink></para></TD><TD><para>I can query to find what mref topics have been changed by reflection.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Design change in progress for s80.</para></TD></tr><tr><TD><para><externalLink><linkText>1389</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1389</linkUri></externalLink></para><para><externalLink><linkText>9729</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=9729</linkUri></externalLink></para></TD><TD><para>Reflection history is available for mref topics.</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>Verification in progress. For Phase 2, detailed change history is only available at the topic level. A roll-up change log is in scope for Phase 3.</para></TD></tr></tbody></table></content><content><para>Phase 2 MRef Bugs</para><table border="1"><thead><tr><TD><para>Bug</para></TD><TD><para>Blocking current?</para></TD><TD><para>Blocking all?</para></TD></tr></thead><tbody><tr><TD><para>FIXED! <externalLink><linkText>11398</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11398</linkUri></externalLink> [CAPS][MREF] stubbing error on reflection update [BingAds blocker][DacFx blocker]</para></TD><TD><para>DacFx and BingAds unblocked. </para></TD><TD><para>No.</para></TD></tr><tr><TD><para>FIXED! <externalLink><linkText>12300</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=12300</linkUri></externalLink> [CAPS][MREF][reflection] Overwrite All Comments should be editable after project setup</para></TD><TD><para>No.</para></TD><TD><para>No.</para></TD></tr><tr><TD><para>FIXED! <externalLink><linkText>12301</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=12301</linkUri></externalLink> [CAPS][MREF][reflection] IsCanonical value should be editable after reflection</para></TD><TD><para>No.</para></TD><TD><para>No.</para></TD></tr><tr><TD><para><externalLink><linkText>11913</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11913</linkUri></externalLink> [CAPS][LOC][MREF][reflection] newly reflected mref topics should have Ready for Localization = TRUE by default</para></TD><TD><para>No.</para></TD><TD><para>No, workaround is to select all topics and bulk reset flag.</para></TD></tr><tr><TD><para><externalLink><linkText>12087</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=12087</linkUri></externalLink> [CAPS][MREF][Reflection] Missing Extension Methods for mscorlib</para><para>Resolved, pending verification.</para></TD><TD><para>Unknown. Teams must check whether migrating projects are affected.</para></TD><TD><para>No, not all projects include extension methods.</para></TD></tr><tr><TD><para>FIXED! <externalLink><linkText>12246</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=12246</linkUri></externalLink> [CAPS][MREF][UI] update language labels in CAPS UI and preview to match published content</para></TD><TD><para>No.</para></TD><TD><para>No. UI issue only – no impact to published content.</para></TD></tr><tr><TD><para><externalLink><linkText>12392</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12392?fullScreen=false</linkUri></externalLink> [CAPS] Reference with Syntax topics must support APIScan attributes for native ref topics</para></TD><TD><para>Unknown.</para></TD><TD><para>Only a blocker for projects with conceptual reference. Fix scheduled for s80.</para></TD></tr></tbody></table></content><content><para>Phase 2 MRef Limitations</para><table border="1"><thead><tr><TD><para>Issue</para></TD><TD><para>Mitigation</para></TD><TD><para>Implementation plan</para></TD></tr></thead><tbody><tr><TD><para>Various customizations for the .Net Class Library (fxref), including versioning, are not supported.</para></TD><TD><para>None; fxref cannot migrate in Phase 2.</para></TD><TD><para>Support for fxref is the top reference priority in Phase 3.</para></TD></tr><tr><TD><para>Platform section configuration via support file is not supported. Support files for configuring this section will not be migrated, and by default, the Platforms section will be empty in CAPS and will not build. </para></TD><TD><para>The Platforms section is available for authoring in CAPS. If this section is critical for a migrating project, the mref vendors can add a token manually as a backlog project (feasibility depends on project size).</para></TD><TD><para><externalLink><linkText>1361</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1361</linkUri></externalLink> </para><para>It is a priority in CAPS to improve the platform/versioning experience. Phase 3 focus is on supporting an automated process for the .NET Class Library, which can hopefully be leveraged by other projects. If additional requirements are identified, they will be added to a later sprint.</para></TD></tr><tr><TD><para>There is no UI yet for excluding ("ripping") entities.</para></TD><TD><list class="bullet"><listItem><para>Support files will be migrated to support ripping in existing projects. </para></listItem><listItem><para>You can continue to create and use ripping files via the Filter functionality.</para></listItem><listItem><para>	EditorBrowsable(Never) is now supported, so product teams can set this attribute to exclude APIs from both IntelliSense and CAPS content.</para></listItem></list></TD><TD><para><externalLink><linkText>1390</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1390</linkUri></externalLink> </para><para>An exclusions UI is in scope for Phase 3, but as a p2 item (may be cut). </para></TD></tr><tr><TD><para>Ripping design change: Entities that are dependencies of documented entities (used as params) cannot be ripped. This is to ensure compliant documentation.</para></TD><TD><para>If your project currently rips entities that are dependencies of documented entities, you will need to document them in CAPS.</para></TD><TD></TD></tr><tr><TD><para>Updates to reflection will not be visually indicated with icons.</para></TD><TD><para>You can use queries to identify updates.</para></TD><TD><para><externalLink><linkText>1387</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1387</linkUri></externalLink> </para><para>Feature is in the backlog, but was cut from Phase 2 and does not meet the bar for Phase 3. Depending on user experience of early adopters, this may or may not be prioritized.</para></TD></tr><tr><TD><para>The global dependencies cache, which facilitates reflection by including many common dependencies, is available but not fully populated and not accessible via the CAPS UI. This means some reflections will require more dependencies than DxStudio, and that users cannot add dependencies themselves to make future reflections faster.</para></TD><TD><para>Reflection still works, it just takes a little longer. And we can file requests with the CAPS team to upload dependencies via the backend.</para></TD><TD><para>UI design for the global dependencies cache is not yet complete, and implementation is not scheduled. Depending on user experience of early adopters, this may or may not be prioritized.</para></TD></tr><tr><TD><para>The undocumented API report is not yet functional in CAPS because the CAPS API is not ready to access the DDUEML file from CAPS storage.</para></TD><TD><para>Writers will have to do more due diligence before publishing. The mref vendors can help with a VTP. For projects with very stringent compliance requirements, this may be a blocker. </para></TD><TD><para>API work will begin in Phase 3.</para></TD></tr><tr><TD><para>Rich query functionality is not complete. Currently you can query for topics last changed by the system, and for topics changed in a particular date range, but more granular queries (e.g. syntax changed, XML comments changed) are not available.</para></TD><TD><para>More detailed information is available in the mref topic history.</para></TD><TD><para>Depending on user experience of early adopters, additional queries may or may not be prioritized.</para></TD></tr><tr><TD><para>Reflection log does not contain full details.</para></TD><TD><para>More detailed information is available in the mref topic history.</para></TD><TD><para><externalLink><linkText>9729</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/9729</linkUri></externalLink>
</para> <para>A more detailed reflection log is in scope for Phase 3. 
</para></TD></tr><tr><TD><para>Rich query functionality is not complete. Currently you can query for topics last changed by the system, and for topics changed in a particular date range, but more granular queries (e.g. syntax changed, XML comments changed) are not available.</para></TD><TD><para>More detailed information is available in the mref topic history.</para></TD><TD><para>Depending on user experience of early adopters, additional queries may or may not be prioritized.</para></TD></tr><tr><TD><para>HxS not available. This may block some F1 processes.</para></TD><TD><para>TBD.</para></TD><TD><para>TBD.</para></TD></tr><tr><TD><para>"Updated by System" status must be manually reset.</para></TD><TD><para>Manually reset the status.</para></TD><TD><para><externalLink><linkText>11438</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/11438</linkUri></externalLink>

</para></TD></tr><tr><TD><para>JScript syntax blocks not available.</para></TD><TD><para> None.</para></TD><TD><para><externalLink><linkText>11405</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/11405?fullScreen=false</linkUri></externalLink>

</para> <para>In scope for Phase 3 as part of detailed reflection log.</para></TD></tr><tr><TD><para>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/11405?fullScreen=false</para></TD><TD><para>Errors are caught during reflection.</para></TD><TD><para><externalLink><linkText>11934</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/11934?fullScreen=false</linkUri></externalLink>
</para><para>
In scope for Phase 3, but p2 (may be cut).</para></TD></tr></tbody></table></content>
        
    </section><section address="ExternalCode">
<title>External code snippets (DDUEML only, for now)</title><content><table border="1"><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD></TD><TD><para>	Snippets stored in GIT repository
</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Preview contains the  code snippets during topic preview (XMetaL and CAPS client)</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Detect changes in Git Repo and sync back to CAPS automatically</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD></TD></tr><tr><TD></TD><TD><para>Display code snippet in CAPS UI.</para><list class="bullet">
<listItem>
<para>The folder structure of code snippet in external code repos</para>
</listItem>
<listItem>
<para>The code snippet entities in CAPS</para>
</listItem><listItem><para>The code source files for that code snippet entity</para></listItem><listItem><para>The different segment of that code snippet source file</para></listItem>
</list></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD></TD></tr></tbody></table></content>
</section><section address="LOC">
        
        <title>Localization</title><content>
            <table border="1"><thead><tr><TD><para>General</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para></para></TD><TD><para>E2E support for conceptual and MREF</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Single or bulk editing for pre-handoff metadata</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Publishing for bilingual conceptual and MREF content</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Publishing based on English version</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Auto publish localized content
</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>	View content metadata per locale</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Complex query via dashboard to search for any status and value of localized assets</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token></para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Query support for localized content</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para><token>StatusYellow</token>
</para></TD><TD><para>TO DO</para></TD></tr><tr><TD><para></para></TD><TD><para>Proof of concept for GFM MD</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD><para>TO DO</para></TD></tr></tbody></table>
        <table border="1"><thead><tr><TD><para>Handoff (small and medium size)</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para></para></TD><TD><para>	Creation of handoff package for marked locales for single topic, multiple topic, or via query</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Configurable assets to include in handoff: All, topic, topic metadata, image, image metadata (ALT Text), token</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Scope handoff by including dependency, translation type, handoff type and view aggregation information per entity per locale before creating a handoff</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Ability to do incremental or force handoff</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD> <para>Create Handoff package based on “Handoff candidate” metadata</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Handoff of art and token only via single, multiple selection, or search</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>View handoff progress</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>View handoff result with success and failure counts
</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Handoff package download</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Handoff manifest with all assets, included in handoff package</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>8905</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=8905</linkUri></externalLink></para></TD><TD><para>Mock handoffs</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 might get cut</para></TD><TD></TD></tr></tbody></table><table border="1"><thead><tr><TD><para>Hand back (small and medium size)</para></TD><TD></TD><TD></TD><TD></TD><TD></TD></tr></thead><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para></para></TD><TD><para>Upload partial or full hand back package per handoff
</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Incremental hand backs</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>View upload and processing progress</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD> <para>View hand back result: status and error list</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Download hand back report</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr><tr><TD><para></para></TD><TD><para>Hand back report includes asset content and metadata version per asset</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD><para></para></TD></tr></tbody></table></content>
        
    </section><section address="Publishing">
<title>Publishing</title><content><table border="1"><thead><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr></thead><tbody><tr><TD></TD><TD><para>	Publish single topic to stage and live</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Option to publish topics, TOC only, or both</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Incremental or forced publishing</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Publishing localized content to stage and live based on English published version</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Support for orphan nodes</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Content retirement workflow for all locales at once 1)	Standard
2)	Redirection to another topic or external topic</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Bulk editing for publishing metadata</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Show publishing progress and status on CAPS client</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Publishing report available from CAPS client</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Search by publishing the last errors and warnings per topic</para></TD><TD></TD><TD></TD><TD></TD></tr><tr><TD></TD><TD><para>Stage and Live URLs shown in CAPS</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Ability to publish all content in a docset regardless of publishing flag status</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>CHM output at the docset level</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Word document output at the docset level</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Markdown publish to MTPS</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para><token>StatusGreen</token></para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>10989</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=10989</linkUri></externalLink></para></TD><TD><para>Save single topics in Word for tech reviews</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>1035</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=1035</linkUri></externalLink></para></TD><TD><para>See build reports  over time</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>6489</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=6489</linkUri></externalLink></para></TD><TD><para>Configuration for broken dependencies to be publishing warnings or errors</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 might get cut</para></TD><TD></TD></tr></tbody></table></content>
</section><section address="UserPerm">
        
        <title>User Permission</title><content>
            <para> User Permission Feature List</para><table border="1"><tbody><tr><TD><para><ui>Feature</ui></para></TD><TD><para><ui>Description</ui></para></TD><TD></TD><TD><para><ui>Status</ui></para></TD><TD><para><ui>How-to</ui></para></TD></tr><tr><TD><para><externalLink><linkText>1102</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1102</linkUri></externalLink></para></TD><TD><para>Leveraged Microsoft Active Directory and https://idweb/ to manage user groups and membership</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Administration</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn880637.aspx</linkUri></externalLink></para><para></para></TD></tr><tr><TD><para><externalLink><linkText>1102</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1102</linkUri></externalLink></para></TD><TD><para>Pre-defined permissions based on tasks</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para><externalLink><linkText>Permissions</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn880645.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para><externalLink><linkText>1102</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/1102</linkUri></externalLink></para></TD><TD><para>	Permission management for administrators</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.</para></TD><TD><para>TODO: finish this page</para><para><externalLink><linkText>Administration</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn880637.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para><externalLink><linkText>12075</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12075</linkUri></externalLink></para></TD><TD><para>Permissions for deletion</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>12076</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12076</linkUri></externalLink></para></TD><TD><para>Permissions for reflection</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>12077</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12077</linkUri></externalLink></para></TD><TD><para>Permissions for managing docsets</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 it might get cut</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>12078</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12078</linkUri></externalLink></para></TD><TD><para>Permissions for managing personal queries</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 it might get cut</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>12079</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/12079</linkUri></externalLink></para></TD><TD><para>Leverage CAPS permissions for external code snippets</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 it might get cut</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>6877</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/6877</linkUri></externalLink></para></TD><TD><para>Select All projects or permission sets with one click when granting permissions</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1) P2 it might get cut</para></TD><TD><para></para></TD></tr><tr><TD><para><externalLink><linkText>6877</linkText><linkUri>https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems/edit/6877</linkUri></externalLink></para></TD><TD><para>Search and find users</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 4 (post-May). It might be implemented in Phase 3 if there is time</para></TD><TD><para></para></TD></tr></tbody></table>
        </content>
        
    </section><section address="MD">
        
        <title> Markdown</title><content>
            <table border="1"><tbody><tr><TD><para>Feature</para></TD><TD><para>Description</para></TD><TD></TD><TD><para>Status</para></TD><TD><para>How-to</para></TD></tr><tr><TD><para></para></TD><TD><para>Create, check out, check in, undo check out</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Save draft to the server</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Topic authoring and preview side by side</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD><para>Full screen editing mode</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD><para>Full screen preview mode</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Authoring toolbar for quick insertion of most-common elements</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD> <para>Floating help tool bar</para><list class="bullet">
<listItem>
<para>Instant Markdown syntax help</para>
</listItem>
<listItem>
<para>In-topic TOC</para>
</listItem><listItem><para>Go to top</para></listItem>
</list></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD></TD><TD><para>Autosaving</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Search and Replace</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Publish to MTPS</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para>TODO</para><para><externalLink><linkText>Authoring in Markdown</linkText><linkUri>https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/dn936507.aspx</linkUri></externalLink></para></TD></tr><tr><TD><para></para></TD><TD><para>Proof of concept for convert DDUE topic to Markdown topic</para></TD><TD><mediaLink>
<image xlink:href="b05a88e7-32a9-461d-abcb-cb321d826276"/>
</mediaLink></TD><TD><para>Implemented and verified.
</para></TD><TD><para></para></TD></tr><tr><TD></TD><TD><para>Proof of concept for Markdown topic localization</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD></TD><TD><para>Support html block in markdown localization for both handoff and handback</para></TD><TD><mediaLink>
<image xlink:href="523c6c07-9b76-48ed-8ab6-b610cc507ab1"/>
</mediaLink></TD><TD><para>
<token>StatusYellow</token></para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>11983</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11983</linkUri></externalLink></para><para><externalLink><linkText>11984</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11984</linkUri></externalLink></para><para><externalLink><linkText>11985</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11985</linkUri></externalLink></para><para><externalLink><linkText>11683</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11683</linkUri></externalLink></para><para><externalLink><linkText>11686</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11686</linkUri></externalLink></para><para><externalLink><linkText>11680</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11680</linkUri></externalLink></para><para><externalLink><linkText>11684</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11684</linkUri></externalLink></para></TD><TD><para>Support for core extensions: token, code snippet, note</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>11677</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11677</linkUri></externalLink></para></TD><TD><para>MD validation upon check-in</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>11321</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11321</linkUri></externalLink></para></TD><TD><para>Spell checker</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr><tr><TD><para><externalLink><linkText>11685</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11685</linkUri></externalLink></para></TD><TD><para>Insert bookmarks</para></TD><TD><mediaLink>
<image xlink:href="6c701048-2ff1-4024-8ca5-f9257746c924"/>
</mediaLink></TD><TD><para>Phase 3 (March 2-May 1)</para></TD><TD></TD></tr></tbody></table>
        <para><externalLink><linkText>11677</linkText><linkUri>https://capservice.visualstudio.com/web/wi.aspx?pcguid=3afc7cea-e643-4785-a32c-e3a73e6f08db&amp;id=11677</linkUri></externalLink></para></content>
        
    </section>
    <section address="UnavailableFeatures">
<title>Unavailable features</title><content><para>The following is a list of functionality that is not implemented in CAPS, available in DxStudio, Other functionality that is not available in CAPS.</para></content><content><para>Locking and unlocking content.</para></content>
</section><relatedTopics/>
</developerConceptualDocument>

