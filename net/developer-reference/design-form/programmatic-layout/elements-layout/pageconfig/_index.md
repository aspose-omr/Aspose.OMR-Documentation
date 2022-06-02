---
weight: 9
date: "2022-05-30"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-forms/pageconfig/
title: PageConfig
description: PageConfig element allows you to break large forms into several pages that are recognized as a single document.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
- page
- sheet
---

This element allows you to break large forms into several pages that are recognized as a single document. Pages must always be top-level elements in the form hierarchy and cannot be nested within other layout elements. The form must include at least one **PageConfig** element.

**PageConfig** element does not have a visual representation and is only used to organize form content.

Generated pages are marked with a special QR code that is automatically added to their margin, even if you do not use the [Barcode](/omr/net/programmatic-forms/elements-barcode/) element. This QR code is used as a page identifier and allows the recognition engine to treat multiple scanned images as one form.

{{% alert color="primary" %}} 

- Even if a printable form is split into multiple pages, it will have a single recognition pattern (.OMR) file.
- At the moment, new pages are not automatically created, even if the content does not fit on one page.

{{% /alert %}}

## Declaration

**PageConfig** element is declared as an instance of [`PageConfig`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config.elements.parents/pageconfig/) class. Reference `Aspose.OMR.Generation.Config.Elements.Parents` namespace to use `PageConfig` types without specifying the fully qualified namespace:

```csharp
using Aspose.OMR.Generation.Config.Elements.Parents;
```

To include **PageConfig** element to the form, add it to the `Children` list of the [top-level `TemplateConfig` object]({{< relref "../../#form-object" >}}).

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				/*
				 * Describe page content here
				 */
			}
		}
	}
};
```

## Allowed child elements

All, except for other **PageConfig** elements.

## **Example**

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				new TextConfig() {
					Name="Biology Quiz: Plants",
					FontSize=16,
					FontStyle=FontStyle.Bold
				},
				new EmptyLineConfig(),
				new AnswerSheetConfig() {
					Name="Plants",
					ElementsCount=90,
					ColumnsCount=3,
					AnswersCount=5
				}
			}
		},
		new PageConfig() {
			Children = new List<BaseConfig>() {
				new TextConfig() {
					Name="Biology Quiz: Animals",
					FontSize=16,
					FontStyle=FontStyle.Bold
				},
				new EmptyLineConfig(),
				new AnswerSheetConfig() {
					Name="Animals",
					ElementsCount=90,
					ColumnsCount=3,
					AnswersCount=5
				}
			}
		}
	}
};
```

![Multi-page form](multi-page.png)
