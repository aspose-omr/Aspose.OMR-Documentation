---
weight: 40
date: "2022-05-30"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-forms/
feedback: OMRNET
aliases:
- /net/programmatic-layout/
title: Building forms programmatically
description: Describe the OMR form directly in the application code.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
---

Aspose.OMR allows you to describe the layout and content of an OMR form directly in the application code. Although it takes much more coding than generating forms from [text](/omr/txt-markup/) or [JSON](/omr/net/programmatic-forms/) sources, this approach works best when you need to design forms with personalized fields such as a respondent's name or a unique QR code.

## Form object

The form is described as an instance of [`TemplateConfig`](https://reference.aspose.com/omr/net/aspose.omr.generation.config/templateconfig) class. All internal elements are nested inside this object.

You must also define at least one page as an instance of [`PageConfig`](https://reference.aspose.com/omr/net/aspose.omr.generation.config.elements.parents/pageconfig/) class.

{{% alert color="primary" %}} 
Reference `Aspose.OMR.Generation.Config` and `Aspose.OMR.Generation.Config.Elements.Parents` namespaces to use `TemplateConfig` and `PageConfig` types without specifying the fully qualified namespace:

```csharp
using Aspose.OMR.Generation.Config;
using Aspose.OMR.Generation.Config.Elements.Parents;
```
{{% /alert %}} 

### Basic form structure

The following code generates an empty single-page OMR form:

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				/*
				 * Describe form content here
				 */
			}
		}
	}
};
```

You can use multiple `PageConfig` objects to separate the content of a large form into several pages.

## Elements

Aspose.OMR offers a wide range of elements that allow you to create forms of any complexity - from a simple ballot to high school exam papers and finance application checklists.

- [Layout](/omr/net/programmatic-forms/elements-layout/)  
  Arrange other elements; define the appearance and design of OMR forms.
- [Questionnaires](/omr/net/programmatic-forms/elements-questionnaire/)  
  Build OMR-ready surveys, ballots, checklists, and similar forms.
- [Answer sheets](/omr/net/programmatic-forms/elements-bubble-matrix/)  
  Populate a form with a grid of bubbles representing answers to an exam, test, or assessment.
- [Barcodes and QR codes](/omr/net/programmatic-forms/elements-barcode/)  
  Add barcodes and QR-codes to personalize or uniquely identify a form.
- [WriteInConfig](/omr/net/programmatic-forms/writeinconfig/)  
  Provide a blank field in which the respondent can hand write some text or draw a picture.

## Examples

Check out [code examples](/omr/net/programmatic-forms/examples/) to see how different elements can be used and combined with each other.
