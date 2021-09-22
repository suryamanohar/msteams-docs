---
title: Deploy your Teams app to Azure
description: Deploying sample Teams application to Azure
ms.localizationpriority: medium
ms.topic: reference
keywords: Microsoft Teams developer samples
---

# Deploy your Teams apps to Azure

This tutorial shows you the steps of deploying your Teams app to Azure using Teams Toolkit.

## Before you begin

Make sure your development environment is set up by installing the Prerequisites.

> [!div class="nextstepaction"]
> [Install Prerequisites](prerequisites.md)

Open an app project in Teams Toolkit. If you haven't created any Teams apps yet, try building the first app.

> [!div class="nextstepaction"]
> [Hello World - Build your first app](../get-started/first-app-react.md)

[!INCLUDE [Provision and Deploy your app on Azure](~/includes/get-started/azure-provisioning-instructions.md)]

<!-- markdownlint-disable MD033 -->
<details>
<summary>Learn what happens when you deployed your app to Azure</summary>

Before deployment, the application has been running locally:

* The backend runs using **Azure Functions Core Tools**.
* The application HTTP endpoint, where Microsoft Teams loads the application, runs locally.

Deployment is a two-step process. You provision the resources on an active Azure subscription, and then deploy or upload the backend and frontend code for the application to Azure.

* The backend, if configured, uses various Azure services, including Azure App Service and Azure Storage.
* The frontend application will be deployed to an Azure Storage account configured for static web hosting.

</details>

## See also

* [Tutorials Overview](code-samples.md)
* [Create a conversational bot app](first-app-bot.md)
* [Create a messaging extension](first-message-extension.md)
* [Code Samples](https://github.com/OfficeDev/Microsoft-Teams-Samples)