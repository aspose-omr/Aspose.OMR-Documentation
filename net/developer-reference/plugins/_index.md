---
weight: 15
date: "2024-02-10"
author: "Vladimir Lapin"
type: docs
url: /net/plugins/
feedback: OMRNET
title: Adding new functionality through plugins
description: How to extend the functionality of Aspose.OMR for .NET engine by incorporating additional features provided through a plugin.
keywords:
- plugin
- extension
- addition
- feature
- enhance
---

Aspose.OMR for .NET functionality can be extended by incorporating additional features provided through a plugin.

{{% alert color="primary" %}} 
Aspose.OMR for .NET plugins are provided as NuGet packages. Refer to [installation instructions](/omr/net/installation/) to learn system requirements and prerequisites.
{{% /alert %}}

## Activating a plugin

To activate features provided through a plugin, use `Aspose.OMR.Api.OmrEngine.AddPlugin()` method:

```csharp
var engine = new OmrEngine();
engine.AddPlugin(new HandwritingPlugin());
```
