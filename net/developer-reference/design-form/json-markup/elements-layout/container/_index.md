---
weight: 10
date: "2025-03-20"
author: "Vladimir Lapin"
type: docs
url: /net/json-markup/container/
aliases:
- /json-markup/container/
feedback: OMRNET
feedback: OMRNET
feedback: OMRNET
title: Container
description: Container element is used to break content into columns and to add a footer to the form.
keywords:
- layout
- markup
- template
- design
- form
- JSON
- container
- columns
- footer
---

This element is used to break content into columns and to add a footer to the form. Nested containers must be placed inside [**Block**](/omr/net/json-markup/block/) elements.

**Container** element does not have a visual representation and is only used to arrange other elements.

![Container-based layout](json-containers.png)

## Declaration

**Container** element is declared as an object with `"element_type": "Container"` property.

Elements displayed inside the **Container**'s columns are provided as an array of objects in the **children** property.

```json
{
	"element_type": "Container",
	"children": [
		/*** put child elements here */
	]
}
```

### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"Container"` (case-insensitive).
**children** | array | [Child elements]({{< ref "#allowed-child-elements" >}}).

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**name** | string | _n/a_ | Used as a reminder of the container's purpose; for example, "_General Chemistry_". You can use the same value for multiple containers.<br />This text is not displayed on the form.
**columns_count** | integer |	1 | The number of columns in the container (1 or more). All columns have the same width regardless of their content.
**columns_proportions** | array | _n/a_ | Overrides the number of columns and sets their relative proportions.<br />The number of columns is determined by the length of the array. Column widths (in percent) are provided as array items. The grand total of all column widths must not exceed 100%.
**container_type** | string | "normal" | Determines whether the container is displayed inside the body of the form (`"normal"`) or as a footer at the bottom of the page (`"footer"`).<br />**Each [Page](/omr/net/json-markup/page/) can only have one footer!**
**block_right_margin** | integer | 40 | Right margin (in pixels) of container's columns.
**block_bottom_margin** | integer | 20 | Bottom margin (in pixels) of nested [**Block**](/omr/net/json-markup/block/) elements.
**block_top_padding** | integer | 20 | Top padding (in pixels) of nested [**Block**](/omr/net/json-markup/block/) elements.
**sync_children_height** | Boolean | false | If set to `true`, all blocks in the container will have the same height, regardless of their content.

## Adding page footer

To add a footer that will appear at the bottom of the page:

1. Create a **Container** object.
2. Set the `container_type` property of the object to `"footer"`.
3. Provide the content of the footer in the `children` property.

## Allowed child elements

- [**Block**](/omr/net/json-markup/block/)
- [**AnswerSheet**](/omr/net/json-markup/answersheet/)
- [**Grid**](/omr/net/json-markup/grid/)
- [**CompositeGrid**](/omr/net/json-markup/compositegrid/)

## **Examples**

Check out the code examples to see how **Container** elements can be used and combined with each other.

### Three-column layout

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Container",
					"name": "Three-column layout",
					"columns_count": 3,
					"children": [
						{
							"element_type": "Block",
							"column": 1,
							"children": [
								{
									"element_type": "Content",
									"name": "First column"
								}
							]
						},
						{
							"element_type": "Block",
							"column": 2,
							"children": [
								{
									"element_type": "Content",
									"name": "Second column"
								}
							]
						},
						{
							"element_type": "Block",
							"column": 3,
							"children": [
								{
									"element_type": "Content",
									"name": "Third column"
								}
							]
						}
					]
				}
			]
		}
	]
}
```

![Three-column container](container-3-column.png)

### Page footer

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Container",
					"container_type": "footer",
					"children": [
						{
							"element_type": "block",
							"children": [
								{
									"element_type": "Paragraph",
									"children": [
										{
											"element_type": "Content",
											"name": "Aspose.OMR Examples",
											"align": "right",
											"font_style": "bold",
											"font-size": 14
										},
										{
											"element_type": "Content",
											"name": "© Aspose Pty Ltd 2022",
											"align": "right",
											"font-size": 10
										}
									]
								}
							]
						}
					]
				}
			]
		}
	]
}
```

![Page footer](container-footer.png)
