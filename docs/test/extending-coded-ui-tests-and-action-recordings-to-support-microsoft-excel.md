---
title: "Extend Coded UI Tests and Action Recordings"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
author: gewarren
---
# Extend coded UI tests and action recordings

The testing framework for coded UI tests and action recordings does not support every possible user interface. It might not support the specific UI that you want to test. For example, you cannot immediately create a coded UI test or an action recording for a Microsoft Excel spreadsheet. However, you can create your own extension to the coded UI test framework that supports your specific UI by taking advantage of the extensibility of the coded UI test framework.

![UI Test Architecture](../test/media/ui_testarch.png)

## Sample extension to test Microsoft Excel

This [blog post](https://blogs.msdn.microsoft.com/gautamg/2010/01/05/3-introducing-sample-excel-extension/) contains a link to a [sample extension](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Components.PostAttachments/00/09/94/38/24/ExcelPluginSample.zip) for the coded UI test framework. You can also view the entire [blog post series for coded UI test extensibility](https://blogs.msdn.microsoft.com/gautamg/2010/01/05/series-on-coded-ui-test-extensibility/).

> [!NOTE]
> The sample is intended for use with Microsoft Excel 2010. It may or may not work with other versions of Excel.

## See also

- <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UITestActionFilter>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage>
- [Use UI automation to test your code](../test/use-ui-automation-to-test-your-code.md)
- [Best practices for coded UI tests](../test/best-practices-for-coded-ui-tests.md)
- [Supported configurations and platforms for coded UI tests and action recordings](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)