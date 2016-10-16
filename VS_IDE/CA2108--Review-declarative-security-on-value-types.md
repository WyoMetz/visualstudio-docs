---
title: "CA2108: Review declarative security on value types"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d62bffdd-3826-4d52-a708-1c646c5d48c2
caps.latest.revision: 16
manager: douge
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# CA2108: Review declarative security on value types
|||  
|-|-|  
|TypeName|ReviewDeclarativeSecurityOnValueTypes|  
|CheckId|CA2108|  
|Category|Microsoft.Security|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A public or protected value type is secured by a [Data and Modeling](../Topic/Data%20and%20Modeling%20in%20the%20.NET%20Framework.md) or [Link Demands](../Topic/Link%20Demands.md).  
  
## Rule Description  
 Value types are allocated and initialized by their default constructors before other constructors execute. If a value type is secured by a Demand or LinkDemand, and the caller does not have permissions that satisfy the security check, any constructor other than the default will fail, and a security exception will be thrown. The value type is not deallocated; it is left in the state set by its default constructor. Do not assume that a caller that passes an instance of the value type has permission to create or access the instance.  
  
## How to Fix Violations  
 You cannot fix a violation of this rule unless you remove the security check from the type, and use method level security checks in its place. Note that fixing the violation in this manner will not prevent callers with inadequate permissions from obtaining instances of the value type. You must ensure that an instance of the value type, in its default state, does not expose sensitive information, and cannot be used in a harmful manner.  
  
## When to Suppress Warnings  
 You can suppress a warning from this rule if any caller can obtain instances of the value type in its default state without posing a threat to security.  
  
## Example  
 The following example shows a library containing a value type that violates this rule. Note that the `StructureManager` type assumes that a caller that passes an instance of the value type has permission to create or access the instance.  
  
 [!CODE [FxCop.Security.DemandOnValueType#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.DemandOnValueType#1)]  
  
## Example  
 The following application demonstrates the library's weakness.  
  
 [!CODE [FxCop.Security.TestDemandOnValueType#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.TestDemandOnValueType#1)]  
  
 This example produces the following output.  
  
 **Structure custom constructor: Request failed.**  
**New values SecuredTypeStructure 100 100**  
**New values SecuredTypeStructure 200 200**   
## See Also  
 [Link Demands](../Topic/Link%20Demands.md)   
 [Data and Modeling](../Topic/Data%20and%20Modeling%20in%20the%20.NET%20Framework.md)