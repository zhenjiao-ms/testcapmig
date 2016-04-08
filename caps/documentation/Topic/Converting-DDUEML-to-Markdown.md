---
title: Converting DDUEML to Markdown
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 140a4edf-d759-4ea6-9cf2-24001a79583a
---
# Converting DDUEML to Markdown
We have a tool for cloning docsets into new portfolios and converting DDUEML to Markdown. There are various reasons why you might clone a docset, and they don't all relate to Markdown, but the tool was originally created to enable testing Markdown conversion in a non-production environment, which is why both functions are in the same UI.

This topic covers the options and workflow for using the tool to convert DDUEML to Markdown, including reporting and test conversion. Information about using the tool to create new versions or move docsets between portfolios is coming soon.

 For access to the tool, contact MBradley for assistance.

## Converting DDUEML to Markdown

Let's walk through the tool options in order of the standard conversion workflow.

### Run a pre-conversion report

Before you start cloning and test converting, you should run a report to clean up known issues in your DDUEML. 

To run a report for the entire portfolio:
1. Open the portfolio and select the top-level Docset node, then copy the URL:
![TopLevelURL](/Image/TopLevelURL.png)
You should see "/docsetsroot/" near the end of the URL.
2. Press enter. Now you see two options:
![1Clone2Convert](/Image/1Clone2Convert.png)
3. Select option 2 for MDConvertTool. This brings up four options:
![ConvertOptions](/Image/ConvertOptions.png)
4. Select option 4 for report only. **Important:** If you select 1 or 2, you may convert accidentally! If you do this in production, people will be displeased. 
5. Now you get a weird question about preferred order of languages. This refers to the preferred language for converting codeEntityReference links to standard Markdown links (in DDUEML, codeEntityReference links render differently depending on the reader's language settings; Markdown doesn't yet have this capability, so links are converted to normal Markdown links, with link text in the first available preferred language, by default C#). You should almost always press enter to select the default. Only select a different order if you are targeting a specific language, such as F# for the F# user guides. 
6. The tool will now resolve the scope and give a topic count. For portfolio level reporting, this should be the total number of topics in the portfolio.
7. If the number looks right and you want to proceed, select Yes + Enter.
8. The mock conversion will run. The language can be a bit frightening because it seems to actually be converting, but if you selected option 4 it will just generate a report. It can take a long time for large numbers of topics. 

To run a report for a single docset:
1. Open the portfolio and select the docset you want.
2. Copy the URL. You should see "docset/" followed by a GUID near the end of the URL (instead of "/docsetsroot/").
3. The rest of the steps are the same as portfolio-level reporting, plus...
4. When the report opens, you should add the docset name to the file name before saving it (the default name just includes the portfolio, not the docset, which is confusing if you run reports for more than one docset.

You can also run a report on a single topic: Just copy the topic URL and use that in the first step. You might do this, for example, to verify that individual skips have been fixed in the source. You should NOT contemplate topic-level conversion in production: The localization overhead would be way too high.

### Review skips and warnings
Topics are skipped for conversion if the conversion tool cannot appropriately handle the DDUEML. For example tables within tables are not supported in Markdown, and content should be intelligently refactored before conversion. Warnings occur when the tool can convert the DDUEML, but some functionality will be lost, or the converted content might not look as expected. For example,  lists are not supported in Markdown tables, so the tool converts lists to lines of plain text with hyphens instead of bullets. The pre-conversion tool lists the skips and warnings you would get it you attempted conversion on the current content, and you may want to edit the content either in the source DDUEML or in Markdown after final conversion.

For skips, you need to fix the source DDUEML content before you can convert to Markdown. For warnings, no action is required, but you should understand what will happen to your content before you convert.

For more details about what happens in conversion and how to fix skips, see [Markdown Conversion Details](Markdown-Conversion-Details.md).

### Clone then test convert

OK! You've run your report, fixed your skips, and reviewed your warnings. You're ready to test convert in Markdown and request automated comparison testing against the DDUEML. To  compare two versions, they need to be in different environments, so the first step is to create a copy of the source DDUEML in the **DevInt partner** test environment via cloning.

1. Paste in your portfolio URL and press enter. Again, this can be a URL at any level of the portfolio, but note that only full portfolios or docsets can be cloned -- not individual topics.
2. Select option 1 for clone tool.
3. Depending on your URL, you will see different options at this point: If you link to a specific docset, the tool will assume you just want that docset and take you to step 4. If you link to the top-level of the portfolio OR to a topic within any docset, the tool will ask which docsets to clone:
   * To clone all docsets in the portfolio, hit enter.
   * To clone one or more docset, type the docset names, separated by comma.
      * Docset names are case sensitive.
	  * Do not include spaces between the names and the commas.
4. If asked, select to convert in the DevInt tenant, in the partner environment (most users will not see these options).
5. Next, you will be asked to specify code snippet repos to clone (if your portfolio uses snippets). For testing purposes, select enter to clone them all.
5. If desired, enter the name for your target portfolio. This can be an existing portolio in the DevInt environment to which you want to move content, or the name you want for a new portfolio. Remember that you must specify a portfolio that already exists in DevInt, not PROD, or a new portfolio will be created for you in DevInt.
    * The default portfolio names follow the format "_sourceName_ Cloned _date_", which is not user friendly, so it is recommended that you specify a name that will be easy to identify later, such as "SQL Drivers Test 1".
6. To add content to an existing portfolio, enter the target portfolio ID. Otherwise press enter for default and a new portfolio will be created.
    * The portfolio GUID is the second GUID in the portfolio URL, e.g. the one in **bold** below:
https://devint.microsoftonedoc.com/#/organizations/ffabd50649854ead8b30a42798aeb2ed/projects/**d83eb9ef-bbff-4f2a-8cca-1ca309830b51**/containers/d31abeea-7047-4302-ad48-ba5b62e8f88e/docsetsroot
   * Again, this must be a URL in DevInt, not PROD. You should see devint.microsoftonedoc.com after https:// in the URL.
7.  Specify the locales to be cloned. 
    * Locales are case-sensitive.
	* For testing, this should be en-US,de-DE,ja-JP.
6. The clone will start now. It takes a while, especially for large content sets!
7. When the clone is complete, the tool will give you the option to convert cloned content immediately to Markdown. Select yes.

### Request automated comparison testing

CSI Global Services has a vendor for automated content comparison testing. To request a test, do the following:
1. Stage the newly converted content. Content from DevInt\partner stages to the PPE environment.
2. Check the publishing report for failures, fix user errors, and try again. For reliable test results, you should have a fully successful stage before requesting testing.
3. Re-stage the source DDUEML content to MSDN or Technet stage.
4. Send an email to Ke Xu with the following information:
    * Source portfolio (a link to DDUEML portfolio)
    * Top-level stage link (a link to the root node on MSDN or Technet stage)
    * Converted portfolio (a link to the Markdown portfolio)
    * Top-level PPE link (a link to the root node on PPE)
    * GUIDs to test (this can be the conversion report, or can be generated via query in CAPS)
5. Ke will send this to the testing vendor and give you an ETA for results. Depending on the size of the content set and the number of projects in the queue, this is generally 1-2 weeks.
6. The vendor will send the results in email when complete.
7. The CSI CE PM team will triage the results to clear out false positives, etc. Content issues will be assigned to you to fix in the source; tool issues will be assigned to VSC.
8. When all bugs are resolved, you can optionally test convert again. Or you can go live.
    

### Convert live

You can't convert live without explicit permission and signoff from Loc. Give Loc at least two weeks' heads up. And when you're ready to convert live, contact the CSI CE PM team.

