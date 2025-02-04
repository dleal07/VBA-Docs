---
title: Comments.Add2 method (PowerPoint)
keywords: vbapp10.chm641005
f1_keywords:
- vbapp10.chm641005
ms.assetid: 4add4727-0193-061b-da71-793a4d6b3aa9
ms.date: 07/14/2020
ms.prod: powerpoint
ms.localizationpriority: medium
---


# Comments.Add2 method (PowerPoint)

Replaces hidden Add method. Returns a **[Comment](powerpoint.comments.add2.md)** object that represents a new comment added to a slide. For more infomation about modern comments, see [Modern comments in PowerPoint](https://support.microsoft.com/office/modern-comments-in-powerpoint-c0aa37bb-82cb-414c-872d-178946ff60ec).

> [!Important]
> This method replaces **[Add()](powerpoint.comments.add.md)** and should be used moving forward. 


## Syntax

_expression_.**Add2** (_Left_, _Top_, _Author_, _AuthorInitials_, _Text_, _ProviderID_, _UserID_)

_expression_ A variable that represents a **[Comments](PowerPoint.Comments.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Left_|Required|**Float**|The position, measured in points, of the left edge of the comment, relative to the left edge of the presentation.|
| _Top_|Required|**Float**|The position, measured in points, of the top edge of the comment, relative to the top edge of the presentation.|
| _Author_|Required|**String**|The author of the comment.|
| _AuthorInitials_|Required|**String**|The author's initials.|
| _Text_|Required|**String**|The comment's text. |
| _ProviderID_|Required|**String**|The service that provides contact information.Example: "AD" (Active Directory)|
| _UserID_|Required|**String**|The ID of the user providing the comment.|

## Return value

 **COMMENT**

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
