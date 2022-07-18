---
weight: 10
date: "2022-05-13"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/page-setup/
title: Page setup
description: How to customize the paper size, orientation, font, images, and other layout settings of a printable form.
keywords:
- render
- page
- form
- print
- paper
- layout
- config
- setup
- sheet
- font
- color
---

The paper size, orientation, font, and other layout settings are configured through [`GlobalPageSettings`](https://reference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object. It also allows you to provide paths to images used in the form. `GlobalPageSettings` object is passed as an optional parameter to the [template generation methods](/omr/net/generate-template/).

## Page setup

You can customize the following page layout parameters through `GlobalPageSettings`:

- [`PaperSize`](https://reference.aspose.com/omr/net/aspose.omr.generation/papersize) - page sizes and dimensions. Default: _A4 (210 x 297 mm)_.
- [`Orientation`](https://reference.aspose.com/omr/net/aspose.omr.generation/orientation) - page orientation. Default: _portrait (vertical)_.
- `PageMarginLeft` and `PageMarginRight` - left and right margins of the page, in pixels.
- `FontFamily` - default font family for all texts, except for those directly overridden in the source code. For example, `"Courier New"`.  
  {{% alert color="primary" %}}
  Make sure the font is installed on the system that generates the printable form!
  {{% /alert %}}
- `FontSize` - default font size for all texts, except for those directly overridden in the source code.
- [`FontStyle`](https://reference.aspose.com/omr/net/aspose.omr.generation/fontstyle) - default font style for all texts, except for those directly overridden in the source code.
- [`BubbleSize`](https://reference.aspose.com/omr/net/aspose.omr.generation/bubblesize) - default size of answer bubbles, except for those directly overridden in the source code.
- [`BubbleColor`](https://reference.aspose.com/omr/net/aspose.omr.generation/color) - color of all bubbles. Default: black.

## Image paths

The `GlobalPageSettings` object is also used to provide the full path to each image mentioned in the [source code](/omr/net/design-form/). The paths are provided as an array of strings using `ImagesPaths` property.

Read more info in this [article](/omr/net/generate-template/images/).

## Example

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	PaperSize = Aspose.OMR.Generation.PaperSize.Tabloid,
	Orientation = Aspose.OMR.Generation.Orientation.Horizontal,
	BubbleColor= Aspose.OMR.Generation.Color.Red,
	ImagesPaths = new string[] {
		@"c:\images\aspose-logo.png",
		@"c:\images\vignette.png"
	}
};
```
