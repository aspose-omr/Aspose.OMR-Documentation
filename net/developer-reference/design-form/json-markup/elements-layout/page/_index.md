---
weight: 9
date: "2022-05-16"
author: "Vladimir Lapin"
type: docs
url: /net/json-markup/page/
feedback: OMRNET
title: Page
description: Page element allows you to break large forms into several pages that are recognized as a single document.
keywords:
- layout
- markup
- template
- design
- form
- JSON
- page
- sheet
---

This element allows you to break large forms into several pages that are recognized as a single document. Pages must always be top-level elements in the form hierarchy and cannot be nested within other layout elements. The [source code]({{< relref "../../#asposeomr-template-structure" >}}) of the form must include at least one **Page** element.

**Page** element does not have a visual representation and is only used to organize form content.

Generated pages are marked with a special QR code that is automatically added to their margin, even if you do not use the [Barcode](/omr/net/json-markup/elements-barcode/) element. This QR code is used as a page identifier and allows the recognition engine to treat multiple scanned images as one form.

{{% alert color="primary" %}} 

- Even if a printable form is split into multiple pages, it will have a single recognition pattern (.OMR) file.
- At the moment, new pages are not automatically created, even if the content does not fit on one page.

{{% /alert %}}

## Declaration

**Page** element is declared as an object with `"element_type": "Page"` property as a child of the [top-level **Template** element]({{< relref "../../#asposeomr-template-structure" >}}). Multiple pages are provided as array items.

```json
{
	"element_type": "Page",
	"children": [
		/*** put child elements here */
	]
}
```

## Allowed child elements

All, except for other **Page** elements.

## **Example**

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Text",
					"name": "Biology Quiz: Plants",
					"font_size": 16,
					"font_style": "bold"
				},
				{
					"element_type": "EmptyLine"
				},
				{
					"element_type": "AnswerSheet",
					"name": "Plants",
					"elements_count": 90,
					"columns_count": 3,
					"answers_count": 5,
				}
			]
		},
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Text",
					"name": "Biology Quiz: Animals",
					"font_size": 16,
					"font_style": "bold"
				},
				{
					"element_type": "EmptyLine"
				},
				{
					"element_type": "AnswerSheet",
					"name": "Animals",
					"elements_count": 90,
					"columns_count": 3,
					"answers_count": 5,
				}
			]
		}
	]
}
```

![Multi-page form](multi-page.png)
