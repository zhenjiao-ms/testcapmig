---
title: How to file a Live Site Issue (LSI)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 468cf100-8e42-47b2-9373-f61ceeb5c2f9
---
# How to file a Live Site Issue (LSI)
File an Issue when you are facing a problem with **CAPS in the production environment**.

In this topic:

-   [Filing a CAPS live site issue from msdnhelp:](#FilingLSI)

-   [Priority description and SLA:](#PriorityAndSLA)

-   [Validating the issue is resolved](#ValidatingLSI)

-   [On Call Rotation](#LSIOnCall)

## <a name="FilingLSI"></a>Filing a CAPS live site issue from msdnhelp:
1)	Open a browser and render http://msdnhelp/ and click on “Customer Impact Issues (aka LSI)” as shown below:

![](../Image/LSIImg1.jpg)

2)	This would take you to the below screen, where you will enter “Title”, and choose “CAPS” from “Application Dropdown”

![](../Image/LSIIMg2.jpg)

3)	Fill in the required details per issue in “Affected Area”, “Issue Severity”, “Description”, “Repro Steps” and click on Submit, as shown below

![](../Image/LSIImg3.jpg)

4)	Once the submit is done, it takes you to the next screen where you can drag and drop any attachments related to issue can be referred and then click on “DONE”

![](../Image/LSIIMg4.jpg)

Once the above step is completed, a TFS work-item is created and assigned to VSCOPS and an email is sent accordingly CCing you on it.

**Note: Please email VSCOPS or ping/mail visuram@ in case of any issues/questions while filing CAPS LSIs from msdnhelp/**

## <a name="PriorityAndSLA"></a>Priority description and SLA:

|Priority|Description|SLA|
|------------|---------------|-------|
|P0|-   CAPS Portal or Service is completely down|-   **Detection** time: 5 mins<br />-   **Response** time: 15 mins<br />-   **Mitigation** time: 4 hours|
|P1|•	Blocks a main business event or release<br /><br />•	Important/Major feature not working and blocking publishing, applies for single user as well<br /><br />•	Publishing doesn’t work or too slow (Example: 10K topics’ publishing is taking more than 2 hours)<br /><br />•	Handoff or Handback (Localization) issues, blocking a release<br /><br />•	Content data loss for entire project (Docset Level) before publishing<br /><br />•	Issues with Page layout at TOC or docset level during publishing<br /><br />•	Any other (code snippets, metadata changes for “multiple topics” etc.) LSI having an End user impact|-   **Detection** time: 1 hour<br />-   **Response** time: 1 business day<br />-   **Mitigation** time: 5 business days|
|P2|•	Single client crashes.<br /><br />•	Intermittent performance issues or content loss at Topic level.<br /><br />•	Failing scenarios with a workaround.<br /><br />•	Single scenarios failure, which is not blocking an event/team<br /><br />•	Performance issues of a specific functionality<br /><br />•	Some tasks that cannot be done via the UI --&gt; Portfolios management, Docsets management,  creating a dump of the content (DDUEML, images, tokens, metadata), etc.,.|-   **Detection** time: 2 hours<br />-   **Response** time: 5 business days<br />-   **Mitigation** time: 15 business days (one sprint)|
|P3/P4|DO NOT USE. Enter a bug instead. See instructions[here](http://msdnhelp/NewRequest.aspx?formid=12).|N/A|

## <a name="ValidatingLSI"></a>Validating the issue is resolved
In the Issue template, we do not have Resolved value. So the way to validate than an issue has been resolved is a bit different.

-   Once the engineering team has solved the issue, the issue will be closed and assigned back to you.

-   You will get an automatic e-mail indicating the issue is solved.

-   Please review and, if you agree, then remove your name from the Assigned To field and add a note indicating you validated the issue is solved.

-   If you do not agree with the resolution, activate it and it will go back to the engineering team.

-   Save the issue.

## <a name="LSIOnCall"></a>On Call Rotation
You can find the current on call person at [here](https://icm.ad.msft.net/imp/CurrentOnCall.aspx?teamId=0&tenantId=20342&incdep=0&incvirt=1&mode=chain).

