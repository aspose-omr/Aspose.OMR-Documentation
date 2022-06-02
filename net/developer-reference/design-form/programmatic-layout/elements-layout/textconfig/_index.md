---
weight: 30
date: "2022-05-30"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-forms/textconfig/
title: TextConfig
description: TextConfig element is used to add one or more lines of text to the form.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
- text
---

This element is used to add a line of text to the form. **TextConfig** elements _cannot be nested within other elements_ - they should always be placed directly in the `Children` list of the [`PageConfig` object](/omr/net/programmatic-forms/pageconfig/).

## Declaration

**TextConfig** element is declared as an instance of [`TextConfig`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config.elements/textconfig/) class. Reference `Aspose.OMR.Generation.Config.Elements` and `Aspose.OMR.Generation.Config.Enums` namespaces to use `TextConfig` types without specifying the fully qualified namespace:

```csharp
using Aspose.OMR.Generation.Config.Elements;
using Aspose.OMR.Generation.Config.Enums;
```

The text displayed in the form is specified in the `Name` property.

```csharp
new TextConfig() {
	Name = "Text goes here"
}
```

### Required properties

Name | Type | Description
---- | ---- | -----------
**Name** | `string` | A line of text displayed in the form.

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**FontFamily** | `string` | "Segoe UI" | The font family for the text.
**FontStyle** | [`FontStyle`](https://apireference.aspose.com/omr/net/aspose.omr.generation/fontstyle/) | `FontStyle.Regular` | The font style for a text.<br />Several font styles can be combined with `\|` operator, for example `FontStyle.Bold \| FontStyle.Italic`.
**FontSize** | `int` | 12 | Font size for the text.
**TextAlignment** | [`AlignmentEnum`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config.enums/alignmentenum/) | `AlignmentEnum.Left` | Horizontal text alignment.

## Allowed child elements

None.

## **Example**

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				new TextConfig() {
					Name = "Once upon a midnight dreary, while I pondered, weak and weary,",
					FontFamily = "Courier New",
					FontStyle = FontStyle.Bold | FontStyle.Italic,
					TextAlignment = AlignmentEnum.Center
				},
				new TextConfig() {
					Name = "Over many a quaint and curious volume of forgotten lore-",
					FontFamily = "Courier New",
					FontStyle = FontStyle.Bold | FontStyle.Italic,
					TextAlignment = AlignmentEnum.Center
				},
				new TextConfig() {
					Name = "While I nodded, nearly napping, suddenly there came a tapping,",
					FontFamily = "Courier New",
					FontStyle = FontStyle.Bold | FontStyle.Italic,
					TextAlignment = AlignmentEnum.Center
				},
				new TextConfig() {
					Name = "As of some one gently rapping, rapping at my chamber door.",
					FontFamily = "Courier New",
					FontStyle = FontStyle.Bold | FontStyle.Italic,
					TextAlignment = AlignmentEnum.Center
				}
			}
		}
	}
};
```

![Text](text.png)
