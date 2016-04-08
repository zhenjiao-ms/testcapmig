---
title: How to run a pre-migration report
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65c3c9b2-5f7d-491d-8d95-cf4b7201f142
---
# How to run a pre-migration report
## File a Work Request to Get a Pre-Migration Report
You can submit a [TFS Work Request](http://vstfcsd:8080/tfs/CSI/Engineering/CSICE/_workItems/create/Work%20Request?%5BCSI.Questions.RequestType%5D=Tools+and+Permissions&%5BCSI.Questions.Task%5D=CAPS+Migration+Report&%5BCSI.Questions.Teams%5D=Engineering) to request a pre-migration report on-demand. Requests made this way are automatically processed and the quickest way to get a report.

## Instructions

Using Notepad.exe (or any other text editor) create a text file that contains a list of the DxStudio projects to be migrated

NOTE: All projects for a report must be in the same Dx database. If you are migrating projects from multiple databases you must run a report for each database.

<br/>
  Format the data in the file using one of the following methods:
```
  Project1,Project2,$Project3,$Project4,Projectn
```
  Or
```
  Project1
  $Project2
  $Project3
  Project4
  $Projectn
```
<br/>

NOTE:Projects must be identified as either source projects or publishing projects so the migration process knows how many docsets need to be created during migration. In the project list, all source project names must begin with a $, otherwise they will be considered publishing projects.

2. Save the file with a .txt extension and no spaces in the filename. Recommend a filename like: PortfolioName_DatabaseName.txt
3. Create a new [Work Request](http://vstfcsd:8080/tfs/CSI/Engineering/CSICE/_workItems/create/Work%20Request?%5BCSI.Questions.RequestType%5D=Tools+and+Permissions&%5BCSI.Questions.Task%5D=CAPS+Migration+Report&%5BCSI.Questions.Teams%5D=Engineering) in the CSI CE TFS (The same place used to file PubDesk work requests)
4. Set the following values in the request:  
   a. Title: Anything you want<br/>
   b. Due Date: Today<br/>
   c. Request Type: CAPS Migration Report<br/>
   d. Team: Engineering<br/>
   e. Product Group: CSI_Cross_Team<br/>
   f. CAPS Migration DB: Select the database with the desired Loc option<br/>
   g. Area: Engineering<br/>
   h. Attach the project list text file you created in Step 1 using the Attachments tab<br/>
5. If you want additional people to receive an email notification when this report is ready add their aliases to the Email CC
6. Save the work request

Within 15 minutes you will start receiving email status on your request via the TFS mail system. The final mail will contain a link to the completed report.

If something causes the request to fail the final mail will contain an error report. In the case of a failure contact the migration team for help if you need help correcting the issue.

The length of time it takes to run your report depends on the database and number of projects in your request. Most reports run in 20-40 minutes. Some of the smaller reports take 10 minutes while some of the larger take mulitple hours.

Once you start getting email notifications from TFS you can check your work request to see the current status of your report.

Note: If you have not received any notification regarding your report in email within an hour, check the status of your request in TFS. The mail system used by TFS may be delayed due to high volumes. Your report may already be done and waiting for you. If you check the ticket it and your report is finished, the ticket history will be updated and contain a link to your report.

## To Request a New Copy of Your Report
After addressing issues in the pre-migration report many users want to see a fresh version of their report in order to verify that the issue counts are going down. If you want to request a new copy of your report using the same project list as your previous request, all you need to do is:
1. Go to the [CSI CE TFS](http://vstfcsd:8080/tfs/CSI/Engineering) and open the Work Request you used for the current version of the report (If you don't remember the TFS item ID, there is a link to the work item in the mail you received from TFS when you got the last report)
2. Change the State from Resolved to Active and save the work item
3. Change the State from Active to Scheduled and save the work item again

This will resubmit your request into the queue. You will be notified via email when your new report is complete and ready for you to view.

NOTE: These steps only apply if you wish to run a new copy of your report using the same project list as the previous report. If you have made any changes to the project list you need to follow the process at the top of this page.
<br/>
<br/>
Also, due to a TFS form update, you may also be prompted to re-enter the CAPS Migration Database.