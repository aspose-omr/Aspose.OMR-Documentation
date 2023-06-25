---
weight: 10
date: "2023-06-23"
author: "Vladimir Lapin"
type: docs
url: /cpp/generate-template/page-setup/
feedback: OMRCPP
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
`PaperSize` | `PaperSize` | A4 (210 x 297 mm) | Physical page dimensions.
`Orientation` | `Orientation` | Portrait (vertical) | Page orientation - horizontal (landscape) or vertical (portrait).
`PageMarginLeft` | `int` | 210 pixels | The size of the left page margin in pixels.
`PageMarginLeft` | `int` | 210 pixels | The size of the right page margin in pixels.
`FontFamily` | `string` | _Default system font_ | Font family for all texts, except for those directly overridden in the source code. For example, `"Courier New"`.<br />The selected font must be installed on the system that generates the printable form! Otherwise, form generation will fail with an exception.
`FontSize` | `int` | 12 | Font size for all texts, except for those directly overridden in the form's source code.
`FontStyle` | `FontStyle` | Regular | Font style for all texts, except for those directly overridden in the source code. See the full list of supported font styles [below](#supported-font-styles).
`BubbleSize` | `BubbleSize` | Normal | Size of answer bubbles, except for those directly overridden in the source code. See the full list of supported bubble sizes [below](#supported-bubble-sizes).
`BubbleColor` | `DrawingColor` | Black | Color of all answer bubbles in the form. See the full list of [supported colors](/omr/cpp/supported-colors/).
`ImagesPaths` | `string[]` | _n/a_ | Full path to each image mentioned in the form's [source code](/omr/net/design-form/).

## Supported paper sizes

The `PaperSize` property controls the paper size of the generated form. All form elements will be re-aligned to best match the selected paper size.

Enumeration | Page dimensions (pixels) | Page dimensions (mm) | Page dimensions (inches)
----------- | ------------------------ | -------------------- | ------------------------
`PaperSize.A4`| 2480 x 3508 | 210 x 297 | 8.3 x 11.7
`PaperSize.Legal` | 2551 x 4205 | 215.9 x 355.6 | 8.5 x 14
`PaperSize.Letter`| 2551 x 3295 | 215.9 x 279.4 | 8.5 x 11
`PaperSize.p8519` | 2551 x 5702 | 215.9 x 482.6 | 8.5 x 19
`PaperSize.p8521` | 2551 x 6302 | 215.9 x 533.4 | 8.5 x 21
`PaperSize.Tabloid` | 3295 x 5102 | 279 x 432 | 11 x 17

{{% alert color="primary" %}} 
The selected paper size does not affect the size of bubbles, images or fonts. Changing the paper size only affects the positioning of elements on the page.
{{% /alert %}} 

## Supported font styles

You can use the following font styles for form texts:

Enumeration | Font face
----------- | ---------
`FontStyle.Regular` | Normal
`FontStyle.Bold` | **Bold / strong**
`FontStyle.Italic` | _Italic / oblique_
`FontStyle.Underline` | <u>Underlined</u>
`FontStyle.Strikeout` | <s>Strikethrough</s>

## Supported bubble sizes

Possible sizes of answer bubbles:

Value | Bubble size
----- | -----------
`BubbleSize.Extrasmall` | 40 pixels
`BubbleSize.Small` | 50 pixels
`BubbleSize.Normal` | 60 pixels
`BubbleSize.Large` | 80 pixels
`BubbleSize.Extralarge` | 100 pixels
