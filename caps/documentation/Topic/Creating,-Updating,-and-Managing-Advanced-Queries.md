---
title: Creating, Updating, and Managing Advanced Queries
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0e2a07b-87cc-453a-9bf5-1987b36ed41a
---
# Creating, Updating, and Managing Advanced Queries
Advanced query lets you set complex query criteria. You can also save your query and reuse it later.

**In this topic**

-   [Team queries](#TeamQuery)

-   [Creating and running a query](#CreateRunQuery)

-   [Types of queries](#QueryTypes)

-   [Understanding the query operators](#QueryOperators)

-   [Choosing desired columns for query results](#ColumnPickerQuery)

-   [Sorting results in query output](#ShortQueryResults)

-   [Exporting a query](#ExportingQuery)

-   [Exporting the query results](#ExportQueryResults)

-   [Renaming a query](#RenamingQuery)

-   [Deleting a query](#DeletingQuery)

## <a name="TeamQuery"></a>Team queries
Team queries are shared among all the team members that have access to the portfolio. If you create a query, any other user who has access to your portfolio can see it and, if they have write access, they might be able to modify it.

## <a name="CreateRunQuery"></a>Creating and running a query
![](../Image/Create-Query-1.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|In the upper left-hand area of the CAPS window, click the **New Query** icon.|
|![](../Image/Numbered-Callouts/callout2.png)|The query editor appears in the CAPS window.|
![](../Image/Create-Query-2.png)

By default, clauses for  **Entity Type**,  **Locale**, **Topic Folder** (not shown above -- it's an old screen shot -- see "Scope by topic folder in the table below"), and  **GUID** are added to the query. **Entity Type**, **Locale**, and **Topic Folder** are mandatory and cannot be removed.

|||
|-|-|
|![](../Image/Numbered-Callouts/callout3.png)|Select a value for **Entity Type**:<br /><br />-   Topic<br />-   Image<br />-   Token<br />-   Handoff<br />-   Hand back|
||Scope by topic folder:<br /><br />1.  Click in the Value field for the Topic Folder clause.<br />2.  Choose the path to scope your query under. The default, Docset, will return results for all docsets in the portfolio. You can drill down to any node in any docset.<br /><br />![](../Image/TopicFolder.png)|
|![](../Image/Numbered-Callouts/callout4.png)|To remove a clause, click on the **X** icon.|
|![](../Image/Numbered-Callouts/callout5.png)|To add another clause, click **Add new clause** or one of the **+** icons.|
|![](../Image/Numbered-Callouts/callout6.png)|To change the **AND/OR** logical operators, the **Field**, **Operator**, and field **Value** for an existing clause, click the down arrow next to the drop-down box.<br /><br />![](../Image/AddNewClause_Query.png)|

|||
|-|-|
|![](../Image/Numbered-Callouts/callout7.png)|To group two or more clauses, click the box next to each clause and then click the **Group selected clauses** icon.<br /><br />![](../Image/Create-Query-3.png)|
![](../Image/Create-Query-4.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout8.png)|To ungroup clauses, click the **Ungroup selected clauses** icon.|
|![](../Image/Numbered-Callouts/callout9.png)|Once you've completed the query, click the **Save Query** icon. A dialog pops up to name the query and select whether to save it as a private or shared query.|
|![](../Image/Numbered-Callouts/callout10.png)|To change the name of an existing query, click the **Save query as** icon, or right-click the query name and select **Rename**.|
|![](../Image/Numbered-Callouts/callout11.png)|Run the query by clicking the **Run query** icon.|
|![](../Image/Numbered-Callouts/callout12.png)|To close the query clauses click on the **X** icon.<br /><br />To show the query clause again, click on the **Edit query** icon. ![](../Image/Edit-query-icon.png)|

## <a name="QueryTypes"></a>Types of queries
There are two types of queries in CAPS: entity queries and dependency queries.

![](../Image/QueryTypes.PNG)

Entity queries return the entities (topics, tokens, images, handoffs, or handbacks, depending on the Entity Type selected) that match the query criteria. New queries are entity queries by default.

Dependency queries allow you to find which topics take a dependency on an entity. See **Finding Dependencies** in [Query Techniques and Examples](../Topic/Query-Techniques-and-Examples.md) .

![](../Image/DependencyQuery.PNG)

## <a name="QueryOperators"></a>Understanding the query operators

|||
|-|-|
|=|Use for *&#42;&#42;full-text search&#42;&#42;*.<br /><br />Used to find an exact match of the **Field** of the entity type you are looking for.|
|&lt;&gt;|Use for *&#42;&#42;full-text search&#42;&#42;*.|
|||
|Contains|Use for *&#42;&#42;full-text search&#42;&#42;* (for string fields).<br /><br />It’s only used for full words and it does not admit any wildcards.|
|Does Not Contain|Use for *&#42;&#42;full-text search&#42;&#42;* (for string fields).|
|Begins With|Use for *&#42;&#42;partial-text search&#42;&#42;* (for string fields).<br /><br />It matches a text field with prefix.<br /><br />So if your query is search for all topics where *Name STARTSWITH “What”*, it will return you topics with title “What’s New”, “What Is Azure”, etc.|
|Wildcard|Use for *&#42;&#42;partial-text search&#42;&#42;* (for string fields).<br /><br />It accepts two special characters:<br /><br />1.  ?<br />2.  &#42;<br /><br />‘?’ matches any single character while ‘&#42;’ matches any number (including zero) characters. So if your query is search for all topics that contain the string "Azu" then you need to look for *Name WILDCARD “&#42;Message&#42;”*a nd CAPS will return topics with title “What is New in Message Analyzer”, “Capturing Message Data”, etc.<br /><br />If you use *Name WILDCARD “Message&#42;”* CAPS will only return those topics which name starts with "Messge"<br /><br />If you use  *Name WILDCARD “Message?”* CAPS will only return those topics like "Message" or "Messages"|
|Under|Use to indicate the location of the asset: under a certain docet, TOC folder, folder, etc.|
|Exists|Use for fields that have some predefined values, like users, locales, etc.|
|&gt;=|Use for date or numeric fields.<br /><br />Searches for fields which value is bigger or equal than the specified value.|
|&gt;|Use for date or numeric fields.<br /><br />Searches for fields which value is bigger than the specified value.|
|&lt;=|Use for date or numeric fields.<br /><br />Searches for fields which value is smaller or equal than the specified value.|
|&lt;|Use for date or numeric fields.<br /><br />Searches for fields which value is smaller than the specified value.|

## <a name="ColumnPickerQuery"></a>Choosing desired columns for query results
By default, the results are presented in a list format via the **Query Editor**.

You will see the results now in a table with different columns. You can remove, add or change the order of the columns by clicking on the **Column Options**button ![](../Image/Query---Customize-columns.png).

## <a name="ShortQueryResults"></a>Sorting results in query output
Click on the header of any column to sort the query results by that column.  Clicking on it once, will sort the results in descending order. Clicking on it again, will sort the results in ascending order. An arrow appears if you click on the header of the column to indicate the sorting.

## <a name="ExportingQuery"></a>Exporting a query
You can export a query as a JSON file to be consumed by another tool or process. For example, Loc and PubDesk tools use these extensively.

To export a query:
1. In the Query Editor, click this icon:
![ExportQuery](/Image/ExportQuery.jpg)
2. The query will download as a JSON file.

## <a name="ExportQueryResults"></a>Exporting the query results

1.  Make sure you are viewing the results in a table view, by selecting **Query Results**.

2.  Click on the **Download to Excel** button.

3.  CAPS will give you a link to download the Excel results.

> [!IMPORTANT]
> In Chrome, you might not see the Excel file getting downloaded. Please go to the address bar right side, and click on the popup blocker. Either download the file from there or always allow popups to be downloaded for CAPS site.

## <a name="RenamingQuery"></a>Renaming a query
1. Right-click the query  and select Rename.
2. Type in the name.
3. Hit enter to save the change.

## <a name="DeletingQuery"></a>Deleting a query
1. Right-click the query and select Delete.
2. Click Yes to confirm.
