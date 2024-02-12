---
weight: 10
date: "2024-02-10"
author: "Vladimir Lapin"
type: docs
url: /net/installation/handwriting/
feedback: OMRNET
title: Handwriting recognition plugin
description: Adding or updating handwriting recognition plugin to your project based on Aspose.OMR for .NET.
keywords:
- install
- update
- NuGet
- package
- plugin
- handwriting
- freehand
---

This plugin adds a handwritten input element to machine-readable forms and extends the recognition functionality of Aspose.OMR engine:

- [text_input](/omr/txt-markup/text_input/) text markup element;
- [text_input](/omr/json-markup/text_input/) JSON markup element;
- [TextInputConfig](/omr/net/programmatic-forms/textinputconfig/) class.

**Aspose.OMR for .NET Handwriting recognition plugin** is distributed as a [NuGet package](https://www.nuget.org/packages/Aspose.OMR.Handwriting). You can either add the package to your existing projects, or install the package without downloading the core library.

{{% alert color="primary" %}}
**Aspose.OMR.Handwriting** plugin is optional. You can use the core library without it; however you will not be able to use the handwriting recognition functionality.
{{% /alert %}} 

## System requirements

- [Aspose.OMR for .NET](https://www.nuget.org/packages/Aspose.OMR) version **24.2.0** or later.
- [Microsoft ONNX Runtime](https://www.nuget.org/packages/Microsoft.ML.OnnxRuntime/) version **1.15.1** or later.

If you are using NuGet Package Manager, these dependencies will be installed automatically.

## Installing with NuGet Package Manager UI

**NuGet Package Manager UI** is the easiest way to install and update Aspose.OMR.Handwriting plugin in your project.

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Project** menu and select **Manage NuGet Packages**.  
   Alternatively, you can right-click the project in **Solution Explorer** and select **Manage NuGet Packages** from the context menu.
3. Switch to **Browse** tab.
4. Type "_Aspose.OMR.Handwriting_" (without quotes) in the search box.
5. Select **Aspose.OMR.Handwriting** package from the list.
6. Click **Install** button.  
   You can select a specific version to be installed. However, it is recommended to always use the [latest compatible version](/omr/net/release-notes/latest/) for new projects.
7. If prompted, confirm changes to the solution.
8. If prompted, accept the license terms for installed packages.

## Installing with NuGet Package Manager Console

**NuGet Package Manager Console** lets you install and update Aspose.OMR for .NET in your project using PowerShell commands.

1. Open your solution or a project in Microsoft Visual Studio.
2. Click **Tools** menu, select **NuGet Package Manager** and click **Package Manager Console**.
3. Execute the command `Install-Package Aspose.OMR.Handwriting` to install the latest version of Aspose.OMR NuGet package.
