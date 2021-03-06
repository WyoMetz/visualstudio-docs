---
title: Publish to App Service on Linux
ms.custom: ""
ms.date: 07/23/2018
ms.technology: vs-ide-deployment
ms.topic: "quickstart"
helpviewer_keywords:
  - "deployment, website"
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
  - "azure"
---
# Publish an ASP.NET Core app to App Service on Linux using Visual Studio

You can use the **Publish** tool to publish ASP.NET Core apps to Azure App Service on Linux.

Deployment to App Service on Linux using the **Publish** tool requires Visual Studio 2017 version 15.7.

[!INCLUDE [quickstart-prereqs-azure-linux](includes/quickstart-prereqs-azure-linux.md)]

## Publish to App Service on Linux

1. In Solution Explorer, right-click the project and choose **Publish** (or use the **Build** > **Publish** menu item).

    ![The Publish command on the project context menu in Solution Explorer](../deployment/media/quickstart-publish.png "Choose Publish")

1. If you have previously configured any publishing profiles, the **Publish** pane appears, in which case select **Create new profile**.

1. In the **Pick a publish target** dialog box, choose **App Service Linux**.

    ![Choose Azure App Service](../deployment/media/quickstart-publish-linux.png "Choose Azure App Service")

1. Select **Publish**. The **Create App Service** dialog box appears. Sign in with you Azure account, if necessary, then the default app service settings populate the fields.

    ![Create App Service](../deployment/media/quickstart-publish-settings-app-service-linux.png "Create Azure App Service")

1. Select **Create**. Visual Studio deploys the app to your Azure App Service, and the web app loads in your browser. The project properties **Publish** pane shows the site URL and other details.

    ![Publish property pane showing a profile summary](../deployment/media/quickstart-publish-app-service-summary.png)

## Next steps

In this quickstart, you learned how to use Visual Studio to create a publishing profile for deployment to App Service on Linux. You may want more information on publishing to Linux using Azure.

> [!div class="nextstepaction"]
> [Linux App Service](/azure/app-service/containers/app-service-linux-intro)
