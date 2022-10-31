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
- [`Wrap`](https://reference.aspose.com/omr/net/aspose.omr.generation/wrap) - wrapping mode:
    - `Aspose.OMR.Generation.WrappingPolicy.None` - disable column wrapping (default);
    - `Aspose.OMR.Generation.WrappingPolicy.Column` - enable automatic column wrapping.
- `RotationPointPosition` - the placement of the rectangular [positioning marker](/omr/net/omr-form-structure/) that is used to detect the page orientation. See details below.

## Image paths

The `GlobalPageSettings` object is also used to provide the full path to each image mentioned in the [source code](/omr/net/design-form/). The paths are provided as an array of strings using `ImagesPaths` property.

Read more info in this [article](/omr/net/generate-template/images/).

## Positioning marker placement

The `RotationPointPosition` property controls the placement of the rectangular [positioning marker](/omr/net/omr-form-structure/) that is used to detect the page orientation. It is provided one of the following values of `Aspose.OMR.Generation.RotationPointPosition` enumerator:

Enumeration | Value | Result
---------- | ----- | ------
`TopLeft1` | 10 | ![Below the top-left square positioning marker](TopLeft1.png)
`TopLeft2` | 11 | ![To the right of the top-left square positioning marker](TopLeft2.png)
`TopRight1` | 20 | ![Below the top-right square positioning marker](TopRight1.png)
`TopRight2` | 21 | ![To the left of the top-left square positioning marker](TopRight2.png)
`BottomLeft1` | 30 | ![Above the bottom-left square positioning marker](BottomLeft1.png)
`BottomLeft2` | 31 | ![To the right of the bottom-left square positioning marker](BottomLeft2.png)
`BottomRight1` | 40 | ![Above the bottom-right square positioning marker](BottomRight1.png)
`BottomRight2` | 41 | ![To the left of the bottom-right square positioning marker](BottomRight2.png)

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
