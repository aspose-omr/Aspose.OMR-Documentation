---
weight: 20
date: "2023-06-06"
author: "Vladimir Lapin"
type: docs
url: /cpp/installation/
feedback: OMRCPP
title: Installation
description: Installing and updating Aspose.OMR for C++ Nuget package.
keywords:
- install
- update
- Nuget
- Microsoft
- package
---

**Aspose.OMR for C++** is distributed as a NuGet package. There is no need to download and install any software - the package can be added to your project directly from Microsoft Visual Studio.

{{% alert color="primary" %}} 
The instructions below describe how to install or update Aspose.OMR for C++ in **Microsoft Visual Studio Community 2019**. The installation process for [other versions](/omr/cpp/system-requirements/) of Visual Studio should be quite similar; refer to [documentation](https://docs.microsoft.com/en-us/previous-versions/visualstudio/) for specific details.
{{% /alert %}} 

## Using NuGet Package Manager UI

**NuGet Package Manager UI** is the easiest way to install and update Aspose.OMR for C++ in your project.

### Installing

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Project** menu and select **Manage NuGet Packages**.  
   Alternatively, you can right-click the project in **Solution Explorer** and select **Manage NuGet Packages** from the context menu.
3. Switch to **Browse** tab.
4. Type "_Aspose.OMR_" (without quotes) in the search box.
5. Select **Aspose.OMR.Cpp** package from the list.
6. Click **Install** button.  
   You can select a specific version to be installed. However, it is recommended to always use the [latest version](/omr/cpp/release-notes/latest/) for new projects.
7. If prompted, confirm changes to the solution.
8. If prompted, accept the license terms for installed packages.

### Updating

{{% alert color="primary" %}} 
Refer to Aspose.OMR for C++ [Release Notes](/omr/cpp/release-notes/) to check if the update might alter the application behavior or require changes to existing code.
{{% /alert %}} 

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Project** menu and click **Manage NuGet Packages**.  
   Alternatively, you can right-click the project in **Solution Explorer** and select **Manage NuGet Packages** from the context menu.
3. Select **Aspose.OMR.Cpp** package from the list.
4. Select the update version and click **Update** button.
5. If prompted, confirm changes to the solution.
6. If prompted, accept the license terms for update packages.

## Using NuGet Package Manager Console

**NuGet Package Manager Console** lets you install and update Aspose.OMR for C++ in your project using PowerShell commands.

### Installing

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Tools** menu, select **NuGet Package Manager** and click **Package Manager Console**.
3. Execute the command `Install-Package Aspose.OMR.Cpp` to install the latest version of Aspose.OMR for C++ NuGet package.

### Updating

{{% alert color="primary" %}} 
Refer to Aspose.OMR for C++ [Release Notes](/omr/cpp/release-notes/) to check if the update might alter the application behavior or require changes to existing code.
{{% /alert %}} 

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Tools** menu, select **NuGet Package Manager** and click **Package Manager Console**.
3. Checks if there are newer versions available for any installed packages by executing a command `Get-Package -updates`. If an update is available, you will see something like this:

   ```
   Id               Versions   Description                                   ProjectName
   --               --------   -----------                                   -----------
   Aspose.OMR.Cpp   {23.2.0}   Aspose.OMR for C++ adds optical mark rec...   ConsoleApp1
   ```
4. Update Aspose.OMR for C++ to the latest version by executing a command `Update-Package Aspose.OMR.Cpp`.  
   
   To update to a specific version, provide its name in the `-Version` parameter . For example: `Update-Package Aspose.OMR.Cpp -Version 23.2.0`.
