---
title: How can I run pre-migration reports?
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.assetid: 74abb73b-df57-466b-b4b1-d29c80bedaf8
---
# How can I run pre-migration reports?
## File a Work Request to Get a Pre-Migration Report
You can submit a [TFS Work Request](http://vstfcsd:8080/tfs/CSI/Engineering/CSICE/_workItems/create/Work%20Request?%5BCSI.Questions.RequestType%5D=Tools+and+Permissions&%5BCSI.Questions.Task%5D=CAPS+Migration+Report&%5BCSI.Questions.Teams%5D=Engineering) to request a pre-migration report on-demand. Requests made this way are automatically processed and the quickest way to get a report.

## Instructions

1. Using Notepad.exe (or any other text editor) create a text file that contains a list of the DxStudio projects to be migrated

  Format the data in the file using one of the following methods:

  Project1,Project2,Project3,Project4,Projectn

  Or

  Project1<br>
  Project2<br>
  Project3<br>
  Project4<br>
  Projectn

2. Save the file with a .txt extension and no spaces in the filename. Recommend a filename like: PortfolioName_DatabaseName.txt
3. Create a new [Work Request](http://vstfcsd:8080/tfs/CSI/Engineering/CSICE/_workItems/create/Work%20Request?%5BCSI.Questions.RequestType%5D=Tools+and+Permissions&%5BCSI.Questions.Task%5D=CAPS+Migration+Report&%5BCSI.Questions.Teams%5D=Engineering) in the CSI CE TFS (The same place used to file PubDesk work requests)
4. Set the following values in the request:<br>
   a. Title: Anything you want<br>
   b. Due Date: Today<br>
   c. Request Type: Tools and Permissions<br>
   d. Task: CAPS Migration Report<br>
   e. Team: Engineering<br>
   f. Product Group: CSI_Cross_Team<br>
   g. CAPS Migration DB: Select the database with the desired Loc option<br>
   h. Area: Eningeering\\CSICE<br>
   i. Attach the project list text file you created in Step 1 using the Attachments tab<br>
5. If you want additional people to receive an email notification when this report is ready add their aliases to the Email CC
6. Save the work request

Within 15 minutes you will start receiving email status on your request via the TFS mail system. The final mail will contain a link to the completed report.

If something causes the request to fail the final mail will contain an error report. In the case of a failure contact the migration team for help if you need help correcting the issue.

The length of time it takes to run your report depends on the database and number of projects in your request. Most reports run in 20-40 minutes. Some of the smaller reports take 10 minutes while some of the larger take mulitple hours.

Once you start getting email notifications from TFS you can check your work request to see the current status of your report.
