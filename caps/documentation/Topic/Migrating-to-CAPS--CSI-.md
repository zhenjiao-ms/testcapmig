---
title: Migrating to CAPS (CSI)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 060150ea-7803-49de-a3dc-14b5c7b4651f
---
# Migrating to CAPS (CSI)
#Migrating Your Content to Caps
This document will help you understand the process of migrating content from DxStudio to CAPS.
It will cover

  * An Overview of the migration process
  * Selecting content to migrate
  * How to prepare for migration
  * What to expect during migration
  * What happens after migration
  * Contacts for more information
  
Overview of the Migration Process
---------------------------------

The migration process is a cooperative effort between the CAPS team (CSICE and Shanghai) and the content teams.

1. Content team selects one or more projects in DxStudio to migrate.
2. Content teams can begin preparing their projects using this <html><a href="https://microsoft.sharepoint.com/teams/STBCSI/e/CAPS/_layouts/OneNote.aspx?id=%2Fteams%2FSTBCSI%2Fe%2FCAPS%2FShared%20Documents%2FCAPS&wd=target%28Adoption.one%7C97A92A0F-CB3A-4149-A9DA-3C877CA44623%2FWork%20CSI%20needs%20to%20do%20before%20migration%7C8192575B-2416-4391-9E9A-2DD73928C34F%2F%29
onenote:https://microsoft.sharepoint.com/teams/STBCSI/e/CAPS/Shared%20Documents/CAPS/Adoption.one#Work%20CSI%20needs%20to%20do%20before%20migration&section-id={97A92A0F-CB3A-4149-A9DA-3C877CA44623}&page-id={8192575B-2416-4391-9E9A-2DD73928C34F}&end">pre-migration checklist</a></html> from the CAPS team.
3. CAPS team runs pre-migration report to look for known issues that may cause problems with the migration process.
4. CAPS team runs test migrations to look for unexpected issues.
5. Content team addresses issues in the content projects called out in the pre-migration report.
6. CAPS team addresses any migration process issues.
7. All teams Iterate on steps 2-5 until the migration report is clear.
8. CAPS team runs the actual migration.
9. Content team verifies content structure in CAPS.
10. Content team verifies ability to publish from CAPS.
11. Content team files ticket with PubDesk to cease publishing from migrated project(s). Instructions can be found <html>
<a href="https://microsoft.sharepoint.com/teams/STBCSI/e/CE/_layouts/15/WopiFrame.aspx?sourcedoc={346b2736-53fa-4ad9-ae6e-b1c8d8540947}&action=edit&wd=target%28%2F%2FProject%20Setup%20and%20Build.one%7C512b2212-5807-4c65-8431-7a4c2a03ced7%2FProject%20Setup%20-%20Build%7Cd14c2a42-b478-42e9-8266-b35cbe9d6c4b%2F%29">here</a>.
</html>

Once these steps are complete, all future publishing for the migrated projects is done from CAPS.

A common question at this point is: What happens to my DxStudio project at this point, am I locked out of it?

Once you have migrated a project to CAPS all future authoring and publishing for that project must be
done via CAPS. The long term plan is to retire the DxPlatform however that is not likely to be a reality
for 1-2 years while we go through the archiving and migration processes. Once you migrate a project to
CAPS the Dx project still exists however it will be archived at that point and all future changes will
be made via CAPS.


Selecting Content to Migrate
----------------------------
Whether or not a project can be migrated depends on a number of factors:

  * The structure of the project within DxStudio (how are topics mapped to the TOC)
  * The schema used to store the content
  * The build types needed to publish the content after migration
  * Localization requirements
  * Special content requirements such as MREF and PowerShell

**Structure**

CAPS is still being built. Not all of the planned features are yet available. Each sprint more features are coming on line. For teams looking to migrate projects right now, we need to determine if the features needed to support a given project are actually available in CAPS. Here is a quick overview of CAPS to help provide context:

----------

Content Structure in CAPS

Topics in CAPS are grouped in *projects*. Unlike Dx, the structure of those projects has no bearing on the structure of the content when it gets published. The published structure in CAPS is determined by creating an *outline* within a project. An outline is associated with a parent node in the TOC and then the structure of the outline determines the structure of the TOC under that parent. Topics get linked to nodes in the outline to determine where they appear in the TOC.

----------

Currently CAPS only supports the ability to link topics within a single project to a given outline. This means that the only projects that can be migrated are projects where all topics are contained within the project (not shared in from outside). The ability to link to topics in other projects is coming, it is just not yet available. The migration process also has limitations related to being able to process projects that contain topics shared in from other projects and topics that are mapped to multiple TOC nodes.  

All of these scenarios are being addressed but the work is not yet completed. Because of this, the current projects being targeted for early migration are smaller, self-contained projects that do not contain any complex cross sharing of topics. The target is to begin being able to support more complex structured projects in the February-March (2015) timeframe. This will be updated as more information becomes available.

**Schema**

Currently CAPS supports publishing DDUEXML based content. Work is being done on the Open Authoring project to support Markdown that may eventually be supported in CAPS. That work is on-going and not yet released. For now the focus is on migrating DDUEXML based projects.

**Reference**

End to end support for managed reference, including DLL reflection, XML comment import, XMetal and web authoring, full publishing functionality, XML IntelliSense builds, and localization, will be available in the February release. Some limitations will apply; in particular, support for custom transforms, support files, or other specialized processing options may not be available until after the February release. This may be a blocker for some projects. To verify that your managed reference project can migrate to the February release please contact Megan Bradley as soon as possible to request a test migration.

PowerShell reference support will not be available in the February release.

Automation for other unmanaged reference, such as REST, JavaScript, and Win32/COM, will not be available in the February release. However, existing conceptual reference can be migrated like any other conceptual content.

**Build Types**

The output formats you need for publishing content once it has been migrated also influences the migration decision. Currently CAPS supports web publishing to TechNet and MSDN. The ability to build CHM files is planned for January with Doc files coming soon after that. If you require one of these formats (or another not listed) make sure you have a clear understanding of when the format you need is planned and base your migration plans accordingly.

**Localization Requirements**

While localization support is available in CAPS, some features are still being developed and refined. If your projects include localized content you will want to make sure you review the migration plan with the localization contact Kris Reynolds.

How to prepare for Migration
----------------------------

1. Select one or more projects to migrate.
2. Request a pre-migration report from the CAPS team. This will list known migration issues discovered in your project.
3. Go through this <html><a href="https://microsoft.sharepoint.com/teams/STBCSI/e/CAPS/_layouts/OneNote.aspx?id=%2Fteams%2FSTBCSI%2Fe%2FCAPS%2FShared%20Documents%2FCAPS&wd=target%28Adoption.one%7C97A92A0F-CB3A-4149-A9DA-3C877CA44623%2FWork%20CSI%20needs%20to%20do%20before%20migration%7C8192575B-2416-4391-9E9A-2DD73928C34F%2F%29
onenote:https://microsoft.sharepoint.com/teams/STBCSI/e/CAPS/Shared%20Documents/CAPS/Adoption.one#Work%20CSI%20needs%20to%20do%20before%20migration&section-id={97A92A0F-CB3A-4149-A9DA-3C877CA44623}&page-id={8192575B-2416-4391-9E9A-2DD73928C34F}&end">pre-migration checklist</a></html> and address any applicable issues.
4. Clean up issues listed in the pre-migration report.
5. Request another report to make sure no issues are found.
6. Schedule training on how to author and publish from CAPS so your team will be ready once the migration is completed.

The clean-up process is the main body of work for preparation. Some examples of clean-up work are:

* Making sure that any content you want migrated is in the proper folders (the Not in build folder will not get migrated)
* Making sure that you identify art you want migrated vs. art that will be disposed of during migration
* clean up bad links
* clean up tokens

**The Pre-migration Report**
    
The pre-migration report is a multi-tabbed Excel workbook. The first tab is a summary of everything
the report looks for, each line representing a specific type of issue. For each type of issue found 
there is an additional tab that contains a detailed list of all instances of that issue to help make 
it as easy as possible for you to locate the problem and fix it.
Pre-migration reports can be run as needed to track progress as issues get cleaned up
    
**Resource Considerations**

Depending on the size of the project and number of issues surfaced in the pre-migration report, there may be a considerable amount of clean-up work to do prior to migration. Teams tend to want to migrate their projects a soon as possible after a release. The theory being that at that point, just after a release, the body of content is fresh and clean, ideal for migration. While this is true, keep in mind that the clean-up process will require writer (and possibly Loc) cycles and usually these people are quite busy running up to a release.


What to Expect During Migration
-------------------------------

There really is not any work that the content teams need to do during the actual migration. The Shanghai engineering team runs the migration operation and content will be available in CAPS on the agreed upon date. The process may take minutes or hours depending on the size of the project. 

What Happens After Migration
----------------------------

The post migration checklist can be found <html><a href="https://microsoft.sharepoint.com/teams/STBCSI/e/CAPS/_layouts/15/WopiFrame.aspx?sourcedoc={878876c1-0838-4b98-8625-1d690130ee38}&action=edit&wd=target%28%2F%2FAdoption.one%7C97a92a0f-cb3a-4149-a9da-3c877ca44623%2FCheck%20list%20for%20after%20migration%7C1dda1437-cc0a-4569-8122-0409a676eeea%2F%29">here</a></html>. 

After migration you will want to do a visual inspection of the project to check for any visible problems. You will also need to file a ticket with PubDesk to stop publishing from the DxPlatform project. If your project has localized content you will want your IPM to file a ticket to stop publishing the localized content from Dx as well. Instructions for filing the PubDesk tickets can be found <html) <a href="https://microsoft.sharepoint.com/teams/STBCSI/e/CE/_layouts/15/WopiFrame.aspx?sourcedoc={346b2736-53fa-4ad9-ae6e-b1c8d8540947}&action=edit&wd=target%28%2F%2FProject%20Setup%20and%20Build.one%7C512b2212-5807-4c65-8431-7a4c2a03ced7%2FProject%20Setup%20-%20Build%7Cd14c2a42-b478-42e9-8266-b35cbe9d6c4b%2F%29">here</a></html>. 

Steps will also need to be taken to migrate data for DevUEMetrix. This process is still being developed and instructions will be available soon.

The last step is to make sure writers have joined the proper aliases and received their CAPS training so they are prepared for publishing in CAPS. Once migration is complete all future publishing for the project is done from CAPS. By the time you reach this point, one or more writers on the team need to be trained and ready to use CAPS.

Contacts for More Information
-----------------------------

* Sandra Aldana Abad (saldana) - CAPS Project Leader
* Megan Bradley (mbradley) - Mref Migration Coordinator
* Dave Keitler (davekri) - CSI Migration coordinator
* Kris Reynolds (krisre) - Localization Migration Coordinator 

