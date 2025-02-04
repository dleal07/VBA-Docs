---
title: Application.BeforePrint event (Publisher)
keywords: vbapb10.chm268435491
f1_keywords:
- vbapb10.chm268435491
ms.prod: publisher
api_name:
- Publisher.Application.BeforePrint
ms.assetid: 4d819aab-726e-ab00-89e0-aedcb62d834e
ms.date: 06/04/2019
ms.localizationpriority: medium
---


# Application.BeforePrint event (Publisher)

Occurs before the publication is printed or previewed.


## Syntax

_expression_.**BeforePrint** (_Doc_, _Cancel_)

_expression_ An expression that returns an **[Application](Publisher.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_Doc_|Required| **Document**|The current publication.|
|_Cancel_|Required| **Boolean**| **False** when the event occurs. If the event procedure sets this parameter to **True**, the publication is not printed when the procedure finishes running.|

## Remarks

The **BeforePrint** event fires only after the document is fully loaded and the onload events have returned. Printing does not occur until the event handler is executed.

For more information about using events with the **Application** object, see [Using events with the Application object](../publisher/Concepts/using-events-with-the-application-object-publisher.md).


## Example

The following Microsoft Visual Basic for Applications (VBA) macro shows how to handle the **BeforePrint** event. It displays a message notifying the user that the document is about to be printed.

```vb
Private Sub pubApplication_BeforePrint(ByVal Doc As Document, Cancel As Boolean ) 
 MsgBox "Printing of " & Doc.Name & " is about to occur ." 
End Sub
```

<br/>

For this event to occur, you must place the following line of code in the General Declarations section of your module.

```vb
Private WithEvents pubApplication As Application
```

<br/>

You then must run the following initialization procedure.

```vb
Public Sub Initialize_pubApplication() 
 Set pubApplication = Publisher.Application 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]