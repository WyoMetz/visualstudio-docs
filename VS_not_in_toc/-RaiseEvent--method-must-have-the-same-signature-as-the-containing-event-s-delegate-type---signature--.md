---
title: "&#39;RaiseEvent&#39; method must have the same signature as the containing event&#39;s delegate type &#39;&lt;signature&gt;&#39;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9db77546-9205-4fd2-baf6-6eb1b46b1f1a
caps.latest.revision: 7
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# &#39;RaiseEvent&#39; method must have the same signature as the containing event&#39;s delegate type &#39;&lt;signature&gt;&#39;
A `Custom Event` declaration must have `RaiseEvent` declaration that has the same signature as the delegate type specified by the custom event's `As` clause.  
  
 For the signatures to match, the `RaiseEvent` declaration and the delegate must have the number of parameters, and the parameters types must match.  
  
 **Error ID:** BC31137  
  
### To correct this error  
  
-   Change the parameters of the `RaiseEvent` declaration to match the parameters of the delegate type.  
  
## Example  
 This example shows a custom event with the correct parameter types for the `RaiseEvent` declaration.  
  
 [!CODE [VbVbalrEventError#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#2)]  
  
## See Also  
 [Event Statement](../Topic/Event%20Statement.md)   
 [RaiseEvent - delete](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Delegate Statement](../Topic/Delegate%20Statement.md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)