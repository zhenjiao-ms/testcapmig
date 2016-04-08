---
title: Mark Topics for Bilingual Publishing
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98333028-934c-4c0e-a0bc-3d24dd169452
---
# Mark Topics for Bilingual Publishing
**In this topic**

-   [What is bilingual publishing?](#Whatisbilingualpublishing)

-   [Mark your topic for bilingual publishing](#Markyourtopic)

-   [Review the bilingual publishing options](#ReviewOptions)

## <a name="Whatisbilingualpublishing"></a>What is bilingual publishing?
Bilingual publishing, formerly known as side-by-side publishing, allows users to publish their localized content along with the same content from the source language.  In CAPS the source language is English.  When a user enables bilingual publishing he or she sets the behavior of the Translation Wiki and also the disclaimer shown in the published topic.  The user chooses the bilingual publishing option from a drop down list from the Set locales workflow in the Localization tab.

## <a name="Markyourtopic"></a>Mark your topic for bilingual publishing
Select the topic you want to mark for bilingual publishing.

![](../Image/Bilingual-Publishing-Topic-Setup.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Select the topic you want to edit.|
Next select the Localization tab and then visually confirm that your topic has its To Be Localized value set to True.  Then click on the Set locales button to launch the workflow.

![](../Image/Bilingual-Publishing-Topic-Setup-2.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout2.png)|Select the **Localization** tab.|
|![](../Image/Numbered-Callouts/callout3.png)|Visually confirm the **To Be Localized** value is True.|
|![](../Image/Numbered-Callouts/callout4.png)|Click on the **Set locales** button.|
In the Set Locales workflow select the translation quality level for your topic, Human Translation or Machine Translation.  The select the locale you wish to localize into from the Locales column.

![](../Image/Bilingual-Publishing-Topic-Setup-3.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout5.png)|Select the translation quality level.  In our example it is  **Human Translation**.|
|![](../Image/Numbered-Callouts/callout6.png)|Select the locale.   In our example it is **de-DE**.|
Choose the bilingual publishing value for your selected locale from the Bilingual Settings column.  A list of the bilingual settings and their values are in a table below.   When you are satisfied with your settings click on the Save button to close the workflow  and save your settings.

![](../Image/Bilingual-Publishing-Topic-Setup-4.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout7.png)|Select the **Bilingual Settings** value for your topic.  In our example it is **MT_QualityEditable**.|
|![](../Image/Numbered-Callouts/callout8.png)|Click on the **Save** button when done.|
CAPS displays the bilingual settings for your topic.  You can take a moment to review your bilingual settings for the topic.

![](../Image/Bilingual-Publishing-Topic-Setup-5.jpg)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout9.png)|**Human Translated Locales**|
|![](../Image/Numbered-Callouts/callout10.png)|The **Bilingual Settings** value selected for your topic per locale.|
|![](../Image/Numbered-Callouts/callout11.png)|The **Bilingual Publish Locales** selected for your topic.|
Remember, you can select more than one topic at a time and use the CAPS bulk editing feature to set the bilingual publishing value on more than one topic at a time.  You can also set the bilingual publishing value for more than one locale at a time.  Each locale can have its own bilingual publishing value if desired.

## <a name="ReviewOptions"></a>Review the bilingual publishing options
The table below displays the Bilingual Publishing Settings values.  If the value is editable then the Translation Wiki funtionality allows for users to add their suggestions.  If it is non-editable then the content is 'read-only'.  The disclaimer will translated into the language of the topic on the web site.

|||||
|-|-|-|-|
|**Metadata Name**|**Description**|**Suggested Display Name**|**Disclaimer Text**|
|MT_QualityNonEditable|Bilingual publishing locale setting value for non-editable human translated content.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Human Translation, Non-Editable|No disclaimer|
|MT_QualityEditable|Bilingual publishing locale setting value for editable human translated content.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Human Translation, Editable|"This content was manually translated to a higher quality standard.  If you wish to further improve the quality of the translation, click the Edit button associated with the sentence that you wish to modify."|
|MT_BetaRecycledContents|Bilingual publishing locale setting value for non-editable human translated content for Beta.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Human Translation for Beta, Non-Editable|"This content is from the previous version of the product."|
|MT_Betacontents|Bilingual publishing locale setting value for non-editable machine translated content for Beta.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Machine Translation for Beta, Non-Editable|"This is machine-translated content that is provided for the Beta release.  A fully translated version of this content will be provided in a future release."|
|MT_NonEditable|Bilingual publishing locale setting value for non-editable machine translated content.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Machine Translation, Non-Editable|"This is machine-translated content."|
|MT_Editable|Bilingual publishing locale setting value for editable machine translated content.  Sets Translation Wiki functionality and disclaimer.|Bilingual Publishing Machine Translation, Editable|"This is machine-translated content that members of the community can edit.  We encourage you to improve the translation by clicking the Edit link associated with any sentence below."|
