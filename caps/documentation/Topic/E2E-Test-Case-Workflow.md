---
title: E2E Test Case Workflow
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 144b1a2f-50cc-4235-a3e3-e4d0b5f0e10e
robots: noindex,nofollow
---
# E2E Test Case Workflow
<?xml version="1.0" encoding="UTF-8"?>
<developerConceptualDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns:xlink="http://www.w3.org/1999/xlink">
    <introduction>
        <para></para>
    </introduction>
    <section>
        <title>E2E Test Case Workflow</title><content/>
        <sections>
            <section>
<title>Authoring</title>
<content></content></section><section>
                <title>1. Author a new topic with XMetal</title>
                <content>
                    
							  <list class="bullet"><listItem><para>Select a project<!--test comment --></para></listItem>
							  <listItem><para>Create a new topic</para></listItem>
							  <listItem><para>Edit the topic with XMetal</para><table><tbody><tr><TD><para>In XMetaL</para></TD><TD><list class="ordered"><listItem><para>Check out</para></listItem><listItem><para>Search and insert image</para></listItem><listItem><para>Search and insert token</para></listItem><listItem><para>Search and insert topic link</para></listItem><listItem><para>Insert common text</para></listItem><listItem><para>Check in</para></listItem></list></TD></tr></tbody></table></listItem><listItem><para>Preview the topic after editing in XMetal</para></listItem></list>						  
						  	
                </content>
            </section><section>
                <title>2. Author a new topic with XMetal undo checkout</title>
                <content>
                    
							  <list class="bullet"><listItem><para>Select a project</para></listItem>
							  <listItem><para>Create a new topic</para></listItem>
							  
					  		  <listItem><para>Edit a topic with XMetal undo checkout</para><table><tbody><tr><TD><para>In XMetaL</para></TD><TD><list class="ordered"><listItem><para>Check out</para></listItem><listItem><para>Search and insert image</para></listItem><listItem><para>Undo checkout</para></listItem><listItem><para>Check in</para></listItem></list></TD></tr></tbody></table></listItem><listItem><para>Preview the topic after editing in XMetal</para></listItem></list>						  
						  	
                </content>
            </section><section DoNotNumber="false">
                <title>         3. BulkEditE2E</title>
                <content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose a project and open an existing Doc Set.</para></listItem>
							  <listItem><para>Open TOC and verify if the content exist.</para></listItem>
							  <listItem><para>Expand one Node with Children and verify.</para></listItem>
							  <listItem><para>Select one node with Toc Title.</para></listItem>
							  <listItem><para>Click 'Select Child Nodes' and verify.</para></listItem>
							  <listItem><para>Remove one key word and input a new key word.</para></listItem>
							  <listItem><para>Save changes and verify if it succeed.</para></listItem>
							  </list>						  
						  	
                </content>
            </section>
								
        
            <section>
                <title>4. EditExistingImageE2E</title>
                <content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Select 'Image' container.</para></listItem>
							  <listItem><para>Search and select an existing image.</para></listItem>
							  <listItem><para>Edit the image metadata and save.</para></listItem>
							  <listItem><para>Replace the first image and verify it.</para></listItem><listItem><para>Click 'add' button to add an image and verify it.</para></listItem><listItem><para>Choose one image to delete and verify.</para></listItem></list>						  
						  	
                </content>
            </section><section>
<title>5. EditExistingTokenE2E</title><content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Select 'Token' container.</para></listItem>
							  <listItem><para>Search and select an existing token.</para></listItem>
							  <listItem><para>Edit the token metadata and save.</para></listItem><listItem><para>Edit the token content and save.</para></listItem><listItem><para>Preview the token to verify it.</para></listItem></list>						  
						  	
                </content>
</section><section>
<title>6. EditExistingTopicE2E</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project and choose an existing docset.</para></listItem>
							  <listItem><para>Search and select an existing topic.</para></listItem>
							  <listItem><para>Edit the topic in web.</para></listItem><listItem><para>Save and preview the topic to verify.</para></listItem><listItem><para>Edit the topic metadata and save.</para></listItem></list></content>
</section><section>
<title>7. EditNewImageE2E</title><content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Select 'Image' container.</para></listItem>
							  <listItem><para>Click 'add' and upload image to create a new image entity.</para></listItem>
							  <listItem><para>Edit the image metadata and save.</para></listItem>
							  <listItem><para>Replace the first image and verify it.</para></listItem><listItem><para>Click 'add' button to add an image and verify it.</para></listItem><listItem><para>Choose one image to delete and verify.</para></listItem><listItem><para>Delete the image entity.</para></listItem></list>						  
						  	
                </content>
</section><section>
<title>8. EditNewTokenE2E</title><content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Select 'Token' container.</para></listItem>
							  <listItem><para>Click 'add' and fill information to create a new image entity.</para></listItem>
							  <listItem><para>Edit the token metadata and save.</para></listItem><listItem><para>Edit the token content and save.</para></listItem><listItem><para>Preview the token to verify it.</para></listItem><listItem><para>Delete the token entity.</para></listItem></list>						  
						  	
                </content>
</section><section>
<title>9. EditNewTopicE2E</title><content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Select an existing docset.</para></listItem>
							  <listItem><para>Click 'add' and fill information to create a new topic entity(currently markdown in test case) .</para></listItem>
							  <listItem><para>Edit the topic in web and save it.</para></listItem><listItem><para>Edit the topic in web and check in it.</para></listItem><listItem><para>Preview the topic to verify.</para></listItem><listItem><para>Edit the metadata and save.</para></listItem><listItem><para>View the edit history to verify.</para></listItem><listItem><para>Delete the topic entity.</para></listItem></list>						  
						  	
                </content>
</section><section>
<title>Docset</title>
<content></content></section><section>
<title>1. CreateDocsetAndEditNodes</title><content>
                    
							  <list class="bullet"><listItem><para>Log in CAPS.</para></listItem>
							  <listItem><para>Choose an existing project.</para></listItem>
							  <listItem><para>Create a new docset.</para></listItem>
							  
							  <listItem><para>Expand and verify 3 sub containers: 'TOC', 'Not in TOC' and 'Retired contents'.</para></listItem><listItem><para>Go to 'TOC' container. Click 'add' and fill information to create a new topic entity(currently Conceptual in test case) .</para></listItem><listItem><para>Context click on the topic, add one topic as a child.</para></listItem><listItem><para>Add one topic before and add one after that topic.</para></listItem><listItem><para>Cut one topic and paste it to another topic, test 3 places: before, after and as child.</para></listItem><listItem><para>Context click on one topic, add one topic reference(choose a existing topic) as a child.</para></listItem><listItem><para>Verify the result.</para></listItem></list>						  
						  	
                </content>
</section><section>
<title>Localization</title>
<content></content></section><section>
<title>1. HandbackTopicE2E</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Select 'Handback' container.</para></listItem><listItem><para>Create a Handback</para><list class="ordered"><listItem><para>Upload ZIP package (topic OR image OR token)</para></listItem><listItem><para>Input title</para></listItem><listItem><para>Click 'Import' butom</para></listItem></list></listItem><listItem><para>View Handback status</para></listItem><listItem><para>Check whether Handback succeeded</para></listItem></list></content>
</section><section>
<title>2. Handoff</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Create Handoff</para><list class="bullet"><listItem><para>Select 'Query' container</para></listItem><listItem><para>New a query to search entities:</para><table>
<tbody><tr><TD></TD><TD><para>Topic</para></TD><TD><list class="ordered"><listItem><para>Use advanced search to find topics to be localized</para></listItem><listItem><para>In query result, click 'Create handoff' to kickoff</para></listItem></list></TD></tr>
<tr><TD><para>OR</para></TD><TD><para>Image</para></TD><TD><list class="ordered"><listItem><para>Use advanced search to find images to be localized</para></listItem><listItem><para>In query result, click 'Create handoff' to kickoff</para></listItem></list></TD></tr><tr><TD><para>OR</para></TD><TD><para>Token</para></TD><TD><list class="ordered"><listItem><para>Use advanced search to find tokens to be localized</para></listItem><listItem><para>In query result, click 'Create handoff' to kickoff</para></listItem></list></TD></tr>
</tbody></table></listItem><listItem><para>Go to query result and select all. </para></listItem><listItem><para>Choose 'Force Handoff' and scope Handoff  . </para></listItem><listItem><para>Input other information and create Handoff. </para></listItem></list></listItem><listItem><para>Go to handoff container, discard the created query.</para></listItem><listItem><para>Check whether Handoff succeeded</para></listItem></list></content>
</section><section>
<title>MRef</title>
<content></content></section><section>
<title>1. CreateSimpleMRef</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Create an docset with type MRef</para></listItem><listItem><para>Navigate to 'Reflection'</para></listItem><listItem><para>Fill in 'Source Path'.</para></listItem><listItem><para>Save and validate, verify if validate succeed.</para></listItem><listItem><para>Run the Mref, verify if it succeed.</para></listItem></list></content>
</section><section>
<title>Publish</title>
<content></content></section><section>
<title>1. PublishExistingDocsetToStagingE2E</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Select one docset and expand it.</para></listItem><listItem><para>Open publish page.</para></listItem><listItem><para>Publish with option 'publish to staging'. And fill in other information.</para></listItem><listItem><para>Click 'Publish' and wait for success.</para></listItem></list></content>
</section><section>
<title>2. PublishNewDocsetE2E</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Create publish articles:</para><list class="bullet"><listItem><para>Create an docset.</para></listItem><listItem><para>Expand and verify 3 sub containers: 'TOC', 'Not in TOC' and 'Retired contents'.</para></listItem><listItem><para>Go to 'TOC' container. Click 'add' and fill information to create a new topic entity(currently Conceptual in test case) .</para></listItem><listItem><para>Context click on the topic, add one topic as a child.</para></listItem><listItem><para>Add one topic before and add one after that topic.</para></listItem><listItem><para>Add one topic with markdown format.</para></listItem></list></listItem><listItem><para>Select docset and publish it to staging.</para></listItem><listItem><para>Wait and verify.</para></listItem><listItem><para>Select docset and publish it to live.</para></listItem><listItem><para>Wait and verify.</para></listItem></list></content>
</section><section>
<title>3. QuickPublishE2E</title><content><list class="bullet"><listItem><para>Use api to modify one article.</para></listItem><listItem><para>Use api to publish one article.</para></listItem><listItem><para>Use api to verify.</para></listItem></list></content>
</section><section>
<title>Search</title>
<content></content></section><section>
<title>1. QuickSearchE2E</title><content><list class="bullet"><listItem><para>Log in CAPS.</para></listItem><listItem><para>Choose an existing project.</para></listItem><listItem><para>Select on docset and open TOC container.</para></listItem><listItem><para>Search a topic with title.</para></listItem><listItem><para>verify result.</para></listItem></list></content>
</section></sections>
    </section>
    <relatedTopics/>
</developerConceptualDocument>
