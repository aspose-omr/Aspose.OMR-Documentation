---
weight: 10
date: "2023-04-20"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/page-setup/
feedback: OMRNET
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

Setting | Type | Default value | Description
------- | ---- | ------------- | -----------
[`PaperSize`](https://reference.aspose.com/omr/net/aspose.omr.generation/papersize) | `Aspose.OMR.Generation.PaperSize` | A4 (210 x 297 mm) | Physical page dimensions.
[`Orientation`](https://reference.aspose.com/omr/net/aspose.omr.generation/orientation) | `Aspose.OMR.Generation.Orientation` | Portrait (vertical) | Page orientation.
`PageMarginLeft` | `int` | 210 pixels | The size of the left page margin in pixels.
`PageMarginLeft` | `int` | 210 pixels | The size of the right page margin in pixels.
`FontFamily` | `string` | Segoe UI | Font family for all texts, except for those directly overridden in the source code. For example, `"Courier New"`.<br />The selected font must be installed on the system that generates the printable form!
`FontSize` | `int` | 12 | Font size for all texts, except for those directly overridden in the source code.
[`FontStyle`](https://reference.aspose.com/omr/net/aspose.omr.generation/fontstyle) | `Aspose.OMR.Generation.FontStyle` | Regular | Font style for all texts, except for those directly overridden in the source code.
[`BubbleSize`](https://reference.aspose.com/omr/net/aspose.omr.generation/bubblesize) | `Aspose.OMR.Generation.BubbleSize` | Normal | Size of answer bubbles, except for those directly overridden in the source code.
[`BubbleColor`](https://reference.aspose.com/omr/net/aspose.omr.generation/color) | `Aspose.OMR.Generation.Color` | Black | [Color](/omr/net/supported-colors/) of all answer bubbles in the form.
[`Overflow`](https://reference.aspose.com/omr/net/aspose.omr.generation/overflow) | `Aspose.OMR.Generation.OverflowActions.<Algorithm>` | Do not clip and wrap elements | How to render elements that do not fit in the parent container.<br />See details [below](#clipping-and-wrapping-elements).
[`RotationPointPosition`](https://reference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings/rotationpointposition/) | `Aspose.OMR.Generation.RotationPointPosition` | Below the top-right square positioning marker | The placement of the rectangular [positioning marker](/omr/net/omr-form-structure/) that is used to detect the page orientation.<br />See details [below](#positioning-marker-placement).
[`WritingSystem`](https://reference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings/writingsystem/) | `Aspose.OMR.Generation.WritingSystems.WritingSystem` | Left-to-right (LTR), Western numbering | [Localization](#form-localization), which affects text direction (LTR or RTL) and item numbering of generated OMR forms.
`ImagesPaths` | `string[]` | _n/a_ | Full path to each image mentioned in the [source code](/omr/net/design-form/).<br />Read more info in this [article](/omr/net/generate-template/images/).
`LongWordHandling` | `Aspose.OMR.Generation.LongWordHandling` | Draw word over element's bounds | How to render very long words that do not fit the parent element's width and cannot be wrapped.<ul><li>`DrawOver` (default) - draw long words until a space or end of line is encountered, even outside the bounds of an element.</li><li>`ThrowException` - throw an exception when rendering the form if the long word does not fit the width of the parent element. The form will not be generated.</li></ul>

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

## Clipping and wrapping elements

When designing OMR forms, you may run into a situation where the element does not fit on the page or inside the parent container. Aspose.OMR for .NET offers flexible handling of these edge cases through the use of `Overflow` page setting.

### Do not clip or wrap content

Overflow content is rendered outside the bounds of the parent element. This can result in content overlapping with other elements or being clipped at page boundaries.

This is the default rendering method.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	Overflow = new Aspose.OMR.Generation.OverflowActions.NoClip()
};
```

![Do not clip content](overflow-noclip.png)

### Hide content outside of parent's bounds

Overflow content will be invisible. Cropping will be done both horizontally and vertically. This may result in some content (images, bubbles, text, and so on) not being presented in the rendered OMR form.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	Overflow = new Aspose.OMR.Generation.OverflowActions.Clip()
};
```

![Do not clip content](overflow-clip.png)


### Wrap content

Content that does not match the parent's bounds will automatically appear in the next column. This rendering method only applies to multi-column layouts and cannot slice monolithic elements such as images and barcodes.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	Overflow = new Aspose.OMR.Generation.OverflowActions.Wrap()
};
```

![Move overlapping content on the next column](overflow-wrap.png)

## Form localization

The `WritingSystem` property controls the text direction (LTR or RTL) and item numbering of generated OMR forms. It is provided as an instance of one of the following classes:

Value | Default | Text direction | Item numbering
----- | ------- | -------------- | --------------
[`Aspose.OMR.Generation.WritingSystems.Western`](https://reference.aspose.com/omr/net/aspose.omr.generation.writingsystems/arabic/) | Yes | Left-to-right (LTR) | Western (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
[`Aspose.OMR.Generation.WritingSystems.Arabic`](https://reference.aspose.com/omr/net/aspose.omr.generation.writingsystems/persian/) | | Right-to-left (RTL) | `useNativeNumber = true` - Eastern Arabic (٠,	 ١, ٢, ٣, ٤, ٥, ٦, ٧, ٨, ٩)<br />`useNativeNumber = false` - Western (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
[`Aspose.OMR.Generation.WritingSystems.Persian`](https://reference.aspose.com/omr/net/aspose.omr.generation.writingsystems/western/) | | Right-to-left (RTL) | `useNativeNumber = true` - Persian (۰, ۱, ۲, ۳, ۴, ۵, ۶, ۷, ۸, ۹)<br />`useNativeNumber = false` - Western (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)

### Arabic answer sheet

Right-to-left answer sheet with Eastern Arabic numbering.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	WritingSystem = new Aspose.OMR.Generation.WritingSystems.Arabic(true)
};
```

![Arabic answer sheet](answersheet_arabic.png)

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
