---
weight: 20
date: "2022-04-28"
author: "Vladimir Lapin"
type: docs
url: /net/json-markup/grid/
title: Grid
description: Grid element generates a matrix of numbered bubbles that are combined into a single answer.
keywords:
- layout
- markup
- template
- design
- form
- JSON
- bubbles
- combine
- merge
---

This element generates a block consisting of numbered bubbles. The block is recognized as a whole, resulting in all marked bubbles forming a single answer.

**Grid** element is an OMR-specific approach to collecting simple numeric data such as a TIN or phone number, or getting an answer to a math test without using optical character recognition (OCR).

![Grid element](json-grid.png)

## Declaration

This element is declared as an object with `"element_type": "Grid"` property.

The maximum number of digits in the combined response is specified in the **sections_count** property.

The number of bubbles for each digit is specified in the **options_count** property.

```json
{
	"element_type": "Grid",
	"sections_count": 7,
	"options_count": 10
}
```

### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"Grid"` (case-insensitive).
**sections_count** | integer | The maximum number of digits in the combined response. Each digit is represented as a line or column of bubbles, depending on the element's **orientation** property.
**options_count** | integer | The number of bubbles for each digit.

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**name** | string | _n/a_ | Used as an element's identifier in recognition results and is displayed as a label on the form.
**align** | string | "left" | Horizontal alignment of **Grid** element: `"left"`, `"center"` or `"right"`.
**orientation** | string | "horizontal" | Element's orientation:<ul><li>`"horizontal"` - each digit is represented as a column of bubbles;</li><li>`"vertical"` - each digit is represented as a row of bubbles.</li></ul>
**header_type** | string | "underline" | The type of the box to be displayed in front of each column / row. This box can be used for hand-writing the answer in addition to marking bubbles.<ul><li>`"underline"` - draw a horizontal line.</li><li>`"square"` - draw a box.</li></ul>
**header_border_size** | integer | 3 | Border width of the box to be displayed in front of each column / row.
**header_border_color** | string | "black" | Border color of the box to be displayed in front of each column / row. Can be picked from the following values: `"Aqua"`, `"Aquamarine"`, `"Black"`, `"Blue"`, `"BlueViolet"`, `"Crimson"`, `"DarkBlue"`, `"DarkGreen"`, `"DarkOrange"`, `"DarkSalmon"`, `"Fuchsia"`, `"Indigo"`, `"Lime"`, `"Red"`, `"Teal"`, `"White"`, `"Gray"`, `"LightGray"`.
**vertical_margin** | integer| 0 | Vertical spacing between the element's lines, in pixels.
**bubble_size** | string | "normal" | Size of bubbles: `"extrasmall"`, `"small"`, `"normal"`, `"large"`, or `"extralarge"`.
**x** | integer | _n/a_ | Set the absolute position of the **Grid** element relative to the left edge of the page.<br />Overrides the value of **align** property.
**y** | integer | _n/a_ | Set the absolute position of the **Grid** element relative to the top edge of the page.
**column** | integer | 1 | The number of the column where the **Grid** element will be placed. Only applicable if **Grid** is placed in a multi-column [**Container**](/omr/net/json-markup/container/) element.

## Allowed child elements

None.

## Examples

Check out the code examples to see how **grid** elements can be used.

### Horizontal grid

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Grid",
					"name": "Convert decimal number 123 to octal",
					"sections_count": 4,
					"options_count": 8,
					"bubble_size": "large",
					"header_type": "square"
				}
			]
		}
	]
}
```

![Horizontal grid example](grid-horizontal.png)

### Vertical grid

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Grid",
					"name": "Phone number",
					"sections_count": 7,
					"options_count": 10,
					"bubble_size": "large",
					"orientation": "vertical"
				}
			]
		}
	]
}
```

![Vertical grid example](grid-vertical.png)
