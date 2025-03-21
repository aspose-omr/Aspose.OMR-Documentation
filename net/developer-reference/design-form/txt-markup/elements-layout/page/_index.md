---
weight: 9
date: "2025-03-20"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/page/
aliases:
- /txt-markup/page/
feedback: OMRNET
feedback: OMRNET
feedback: OMRNET
title: page
description: Page element allows you to break large forms into several pages that are recognized as a single document.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- page
- sheet
---

This element allows you to break large forms into several pages that are recognized as a single document. Pages must always be top-level elements in the form hierarchy and cannot be included into other elements.

**Page** element does not have a visual representation and is only used to organize form content.

Generated pages are marked with a special QR code that is automatically added to their margin, even if you do not use the [**barcode**](/omr/net/txt-markup/elements-barcode/) element. This QR code is used as a page identifier and allows the recognition engine to treat multiple scanned images as one form.

{{% alert color="primary" %}} 

- Even if a printable form is split into multiple pages, it will have a single recognition pattern (.OMR) file.
- If you do not add the **page** element, the entire content of the form will be placed on one page.
- At the moment, new pages are not automatically created, even if the content does not fit on one page.

{{% /alert %}}

## Syntax

The element declaration begins with `?page=[name]` statement and ends with `&page` statement. These statements must be placed on separate lines.

`name` attribute is used as a reminder of the page's purpose; for example, "_Page 1_". This is an optional attribute - you can use the same **name** for multiple pages or just omit it. The page name is not displayed on the form.

{{% alert color="primary" %}} 
If you use pages, include all other elements in them. Elements outside of **page** elements will not be rendered.
{{% /alert %}}

### Attributes

The **page** element can be customized by adding optional attributes to it.

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?page=` statement or another attribute, and must begin with a **tab character**.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**orientation** | _Portrait_ | Override individual page orientation: <ul><li>`Horizontal` - landscape</li><li>`Vertical` - portrait</li></ul> | `orientation=Horizontal`
**paper_size** | _A4_ | Override the physical dimensions for the individual page.<br />See details [below](#supported-paper-sizes). | `paper_size=Letter`
**left_margin** | 210 pixels | Override the size of the left page margin in pixels. | `left_margin=120`
**right_margin** | 210 pixels | Override the size of the right page margin in pixels. | `right_margin=120`
**rotation_point_position** | _Below the top-right square reference point marker._ | Override the placement of the rectangular rotation marker that is used to detect the page orientation.<br />See details [below](#rotation-marker-placement). | `rotation_point_position=BottomRight1`

#### Supported paper sizes

The `paper_size` attribute controls the paper size of the generated form. All form elements will be re-aligned to best match the selected paper size.

Enumeration | Page dimensions (pixels) | Page dimensions (mm) | Page dimensions (inches)
----------- | ------------------------ | -------------------- | ------------------------
`A3` | 3508 x 4961 | 297 x 420 | 11.7 x 16.5
`A4`| 2480 x 3508 | 210 x 297 | 8.3 x 11.7
`Legal` | 2551 x 4205 | 215.9 x 355.6 | 8.5 x 14
`Letter`| 2551 x 3295 | 215.9 x 279.4 | 8.5 x 11
`p8519` | 2551 x 5702 | 215.9 x 482.6 | 8.5 x 19
`p8521` | 2551 x 6302 | 215.9 x 533.4 | 8.5 x 21
`Tabloid` | 3295 x 5102 | 279 x 432 | 11 x 17

{{% alert color="primary" %}} 
The selected paper size does not affect the size of bubbles, images or fonts. Changing the paper size only affects the positioning of elements on the page.
{{% /alert %}} 

#### Rotation marker placement

The `rotation_point_position` attribute controls the placement of the rectangular rotation marker that is used to detect the page orientation:

Enumeration | Result
----------- | ------
`TopLeft1` | ![Below the top-left square reference point marker](TopLeft1.png)
`TopLeft2` | ![To the right of the top-left square reference point marker](TopLeft2.png)
`TopRight1` | ![Below the top-right square reference point marker](TopRight1.png)
`TopRight2` | ![To the left of the top-left square reference point marker](TopRight2.png)
`BottomLeft1` | ![Above the bottom-left square reference point marker](BottomLeft1.png)
`BottomLeft2` | ![To the right of the bottom-left square reference point marker](BottomLeft2.png)
`BottomRight1` | ![Above the bottom-right square reference point marker](BottomRight1.png)
`BottomRight2` | ![To the left of the bottom-right square reference point marker](BottomRight2.png)

## Allowed child elements

All, except for other **page** elements.

## **Example**

```
?page=
?text=Biology Quiz: Plants
	font_size=16
	font_style=bold
?empty_line=
?answer_sheet=Plants
	columns_count=3
	elements_count=90
	answers_count=5
&page
?page=
?text=Biology Quiz: Animals
	font_size=16
	font_style=bold
?empty_line=
?answer_sheet=Animals
	columns_count=3
	elements_count=90
	answers_count=5
&page
```

![Multi-page form](multi-page.png)
