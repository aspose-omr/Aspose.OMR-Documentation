---
weight: 20
date: "2022-04-14"
author: "Vladimir Lapin"
type: docs
url: /net/installation/
feedback: OMRNET
title: Installation
description: Adding or updating Aspose.OMR for .NET NuGet package in your project.
keywords:
- install
- update
- NuGet
- package
---

**Aspose.OMR for .NET** is distributed as a NuGet package. There is no need to download and install any software - the package can be added to your project directly from Microsoft Visual Studio.

{{% alert color="primary" %}} 

The instructions below describe how to install or update Aspose.OMR for .NET in **Microsoft Visual Studio Community 2019**. The installation process for [other versions](/omr/net/system-requirements/) of Visual Studio should be quite similar; refer to [documentation](https://docs.microsoft.com/en-us/previous-versions/visualstudio/) for specific details.

{{% /alert %}} 

## Using NuGet Package Manager UI

**NuGet Package Manager UI** is the easiest way to install and update Aspose.OMR for .NET in your project.

### Installing

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Project** menu and select **Manage NuGet Packages**.  
   Alternatively, you can right-click the project in **Solution Explorer** and select **Manage NuGet Packages** from the context menu.
3. Switch to **Browse** tab.
4. Type "_Aspose.OMR_" (without quotes) in the search box.
5. Select **Aspose.OMR** package from the list.
6. Click **Install** button.  
   You can select a specific version to be installed. However, it is recommended to always use the [latest version](/omr/net/release-notes/latest/) for new projects.
7. If prompted, confirm changes to the solution.
8. If prompted, accept the license terms for installed packages.

### Updating

{{% alert color="primary" %}} 

Refer to Aspose.OMR for .NET [Release Notes](/omr/net/release-notes/) to check if the update might alter the application behavior or require changes to existing code.

{{% /alert %}} 

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Project** menu and click **Manage NuGet Packages**.  
   Alternatively, you can right-click the project in **Solution Explorer** and select **Manage NuGet Packages** from the context menu.
3. Select **Aspose.OMR** package from the list.
4. Select the update version and click **Update** button.
5. If prompted, confirm changes to the solution.
6. If prompted, accept the license terms for update packages.

## Using NuGet Package Manager Console

**NuGet Package Manager Console** lets you install and update Aspose.OMR for .NET in your project using PowerShell commands.

### Installing

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Tools** menu, select **NuGet Package Manager** and click **Package Manager Console**.
3. Execute the command `Install-Package Aspose.OMR` to install the latest version of Aspose.OMR NuGet package.

### Updating

{{% alert color="primary" %}} 

Refer to Aspose.OMR for .NET [Release Notes](/omr/net/release-notes/) to check if the update might alter the application behavior or require changes to existing code.

{{% /alert %}} 

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Tools** menu, select **NuGet Package Manager** and click **Package Manager Console**.
3. Checks if there are newer versions available for any installed packages by executing a command `Get-Package -updates`. If an update is available, you will see something like this:

   ```
   Id           Versions   Description                                   ProjectName
   --           --------   -----------                                   -----------
   Aspose.OMR   {22.3.0}   Aspose.OMR for .NET is a standalone .NET l... ConsoleApp1
   ```
4. Update Aspose.OMR for .NET to the latest version by executing a command `Update-Package Aspose.OMR`.  
   
   To update to a specific version, provide its name in the `-Version` parameter . For example: `Update-Package Aspose.OMR -Version 22.2.0`.
