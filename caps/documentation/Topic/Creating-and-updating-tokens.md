---
title: Creating and updating tokens
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e3a8c645-eb75-4926-ac07-43ba3c1827a1
---
# Creating and updating tokens
Tokens can be used for both DDUEML and Markdown content. Note that if you are using a token with XML or HTML tagging, check-in will fail for Markdown topics.

**In this topic:**

-   [Creating a token](#CreatingToken)

-   [Updating the token definition](#UpateTokenDefinition)

-   [Token definitions for DDUEML](#ExampleTokenDefinitionDDUEML)

-   [Token definitions for Markdown](#ExampleTokenDefinitionMD)

## <a name="CreatingToken"></a>Creating a token
![](../Image/defineToken_1.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Click the **Token** section within your portfolio.|
|![](../Image/Numbered-Callouts/callout2.png)|Click on the **+** icon to add the token.|
![](../Image/defineToken_2.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout3.png)|Give a unique name to the token.|
|![](../Image/Numbered-Callouts/callout4.png)|Click **Create**.<br /><br />Next, you'll give the new token a value.|

## <a name="UpateTokenDefinition"></a>Updating the token definition
![](../Image/defineToken_3.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout5.png)|Click **Edit**.|
![](../Image/defineToken_4.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout6.png)|Give the token a value (see [Token definitions for DDUEML](#ExampleTokenDefinition)or [Token definitions for Markdown](#ExampleTokenDefinitionMD)).|
|![](../Image/Numbered-Callouts/callout7.png)|**Check in** your changes when done or...|
|![](../Image/Numbered-Callouts/callout8.png)|**Undo check out** to abandon your changes.|

## <a name="ExampleTokenDefinitionDDUEML"></a>Token definitions for DDUEML

|Type|Example|
|--------|-----------|
|Simple (text strings)|![](../Image/simpleToken.png)|
|Nested (be sure to qualify the tag's namespace (e.g. **&lt;maml:token&gt;**)|![](../Image/nestedTokens.png)|
|Complex DDUEXML (create the tags in XMetal, then cut and paste into the token definition)|![](../Image/complexTokens.png)|
> [!IMPORTANT]
> Complex DDUEXML tokens, when inserted at the wrong point of your topic, will cause schema validation errors.  Be cautious with complex token usage.

## <a name="ExampleTokenDefinitionMD"></a>Token definitions for Markdown
For Markdown, you need to strip out the XML code that comes with the token, i.e., remove *&lt;Token xmlns:xlink="http://www.w3.org/1999/xlink"&gt;&lt;/Token&gt;*. Then, add the token text.

## See also

-   [Grouping assets](../Topic/Grouping-assets.md)

-   [Deleting and Restoring content](../Topic/Deleting-and-Restoring-content.md)

