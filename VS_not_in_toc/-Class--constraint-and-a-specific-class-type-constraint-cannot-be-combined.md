---
title: "&#39;Class&#39; constraint and a specific class type constraint cannot be combined"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 218a7f0c-dd4f-4086-a52c-e8d581377e8b
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
# &#39;Class&#39; constraint and a specific class type constraint cannot be combined
A constraint list includes both the [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7) constraint and the name of a defined class.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. You can specify the following requirements in any combination:  
  
-   The type argument must implement one or more interfaces  
  
-   The type argument must inherit from at most one class  
  
-   The type argument must expose a parameterless constructor that the creating code can access (include the `New` constraint)  
  
 If you do not include any specific class or interface in the constraint list, you can impose a more general requirement by specifying one of the following:  
  
-   The type argument must be a value type (include the `Structure` constraint)  
  
-   The type argument must be a reference type (include the `Class` constraint)  
  
 You cannot specify both `Structure` and `Class` for the same type parameter, and you cannot specify either one more than once.  
  
 **Error ID:** BC32107  
  
### To correct this error  
  
-   If you want to allow the type argument to be any reference type, remove the class name from the constraint list.  
  
-   If you want the type argument to inherit from the specified class name, remove the `Class` keyword from the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)