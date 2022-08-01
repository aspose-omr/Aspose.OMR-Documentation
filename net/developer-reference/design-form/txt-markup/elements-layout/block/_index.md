---
weight: 20
date: "2022-04-21"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/block/
title: block
description: Block element is used to organize content within containers.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- block
- columns
---

This element is used to organize content within [**containers**](/omr/net/txt-markup/container/). Blocks can only be nested within [**container**](/omr/net/txt-markup/container/) elements.

Blocks may not have a visual representation or have a border around them.

![Block layout](blocks.png)

## Syntax

The element declaration begins with `?block=[name]` statement and ends with `&block` statement. These statements must be placed on separate lines.

`name` property is used as a reminder of the block's purpose; for example, "_First column_". This is an optional property - you can use the same **name** for multiple blocks or just omit it. The name is not displayed on the form.

{{% alert color="primary" %}} 

Never add empty lines after the opening `?block=` statement. Doing so will result in an error when rendering a form.

{{% /alert %}}

### Attributes

The **block** element can be customized by adding optional attributes to it.

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?block=` statement or another attribute, and must begin with a **tab character**.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**column** | 1 | The number of the column in which the **block** will be placed.<br />This number must not exceed the number of columns of the parent [**container**](/omr/net/txt-markup/container/) element. | `column=2`
**border** | none | Whether to draw a border around the block.<ul><li>`none` - no border.</li><li>`square` - draw a rectangular border.</li><li>`rounded` - draw a rectangular border with rounded corners.</li></ul> | `border=square`
**border_size** | 3 | Width of the block borders. | `border_size=10`
**border_color** | black | Color of the block borders. Can be picked from the following values: `Aqua`, `Aquamarine`, `Black`, `Blue`, `BlueViolet`, `Crimson`, `DarkBlue`, `DarkGreen`, `DarkOrange`, `DarkSalmon`, `Fuchsia`, `Indigo`, `Lime`, `Red`, `Teal`, `White`, `Gray`, `LightGray`. | `border_color=red`
**is_clipped** | false | If set to `true`, the content of the block is stored to [Images](https://reference.aspose.com/omr/net/aspose.omr.model/recognitionresult/properties/images) collection during recognition, similar to the [**write_in**](/omr/net/txt-markup/write_in/) element. The image can be can be passed to optical character recognition library, such as [Aspose.OCR](https://products.aspose.app/ocr), or saved.<br />If the block contains OMR elements, they will be recognized even if this attribute is set to `true`. | `is_clipped=true`

## Allowed child elements

All, except for **block**.

## **Examples**

Check out the code examples to see how **block** elements can be used and combined with each other.

### Two-column layout

```
?container=Two-column
	columns_count=2
?block=Column 1-1
	column=1
	border=none
?paragraph=
?content=First column, first block.
&paragraph
&block
?block=Column 1-2
	column=1
	border=square
?paragraph=
?content=First column, second block.
&paragraph
&block
?block=Column 2
	column=2
	border=square
	border_size=10
	border_color=blue
?paragraph=
?content=Second column, first block.
&paragraph
&block
&container
```

![Two-column layout](block-two-column.png)

### Fake table layout

```
?container=Two-column
	columns_count=2
	block_right_margin=0
	block_bottom_margin=0
	block_top_padding=0
?block=
	column=1
	border=square
?content=Row 1, cell 1
&block
?block=
	column=1
	border=square
?content=Row 1, cell 2
&block
?block=
	column=2
	border=square
?content=Row 2, cell 1
&block
?block=
	column=2
	border=square
?content=Row 2, cell 2
&block
&container
```

![Fake table layout with container and blocks](fake-table.png)
