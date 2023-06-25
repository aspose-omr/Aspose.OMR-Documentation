---
weight: 20
date: "2023-06-23"
author: "Vladimir Lapin"
type: docs
url: /cpp/design-form/json-markup/
feedback: OMRCPP
title: JSON markup
description: Use the most popular data interchange format for describing machine-readable forms as nested data structures.
keywords:
- layout
- markup
- template
- design
- form
- JSON
---

{{% alert color="caution" %}} 
The current version of Aspose.OCR for C++ has limited support for text markup elements and attributes. Stay tuned for further updates.
{{% /alert %}} 

[JSON](https://www.json.org/json-en.html) is an open standard format widely used in software development and web. Aspose.OMR for C++ allows you to use it to describe the content and layout of forms.

While JSON notation is not as compact as the [text markup](/omr/cpp/design-form/txt-markup/), but it is much easier to read and edit, especially when it comes to complex nested layouts. It supports syntax highlighting, automatic formatting, and code folding in all popular code editors.

According to the [**The JavaScript Object Notation (JSON) Data Interchange Format** specification](https://datatracker.ietf.org/doc/html/rfc8259), it is highly recommended to use **UTF-8** encoding without BOM (byte order mark).

## Core concepts of JSON notation

JSON stands for _JavaScript Object Notation_. As the name suggest, its syntax is similar to the code for creating JavaScript objects:

- Data is provided in form of name / value pairs (**properties**) separated by commas.  
  The **name** must be enclosed in double quotes. The **value** can be one of the following data types:
    - string,
    - number / integer,
    - Boolean,
    - object,
    - array,
    - null.
- An **object** is the collection of properties enclosed in curly braces. Objects can be nested inside other objects.
- An **array** is a comma-separated set of values enclosed in curly braces.
- The top-level object declaration is written as curly brackets that enclose other content.

```json
{
	"element": {
		"name": "value",
		"array": [1, 2, 3],
		"nesting": {
			"name": "Nested object"
		}
	},
	"is_json": true
}
```

## Aspose.OMR template structure

The top-level element of the Aspose.OMR for C++ source code must always be an object with the following structure:

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				/*** put content elements here */
			]
		}
	]
}
```

Content elements are provided as objects with the following set of properties:

- Type of the element is specified in the value of **element_type** property (required).  
- Element attributes are provided as properties with the corresponding names.  
- Nested elements (if any) are passed as objects in the **children** array.

```json
"element_type": "Container"
"children": [
	{
		"element_type": "Block",
		"children": [
			{
				"element_type": "Content",
				"name": "Getting started with JSON markup"
			}
		]
	}
]
```

{{% alert color="primary" %}} 
Aspose.OMR for C++ ignores properties with unsupported names. You can use it to add extra data to the template source that will be processed by other parts of the program code.
{{% /alert %}}

## Elements

Aspose.OMR for C++ offers a wide range of elements that allow you to create forms of any complexity - from a simple ballot to high school exam papers and finance application checklists.

- [Layout](/omr/json-markup/elements-layout/)  
  Arrange other elements; define the appearance and design of OMR forms.
- [Questionnaires](/omr/json-markup/elements-questionnaire/)  
  Build OMR-ready surveys, ballots, checklists, and similar forms.
- [Answer sheets](/omr/json-markup/elements-bubble-matrix/)  
  Populate a form with a grid of bubbles representing answers to an exam, test, or assessment.
- [Barcodes and QR codes](/omr/json-markup/elements-barcode/)  
  Add barcodes and QR-codes to personalize or uniquely identify a form.
- [Write-ins](/omr/json-markup/writein/)  
  Provide a blank field in which the respondent can hand write some text or draw a picture.

## Examples

Check out [code examples](/omr/json-markup/examples/) to see how different elements can be used and combined with each other.
