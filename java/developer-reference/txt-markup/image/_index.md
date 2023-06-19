---
weight: 50
date: "2023-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/design-form/image/
aliases:
- /java/images/
title: Image
feedback: OMRJAVA
description: A markup element that adds a picture to a generated form.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- image
- picture
---

This element is used to insert an image into the form at the provided coordinates.

## Syntax

The element is declared with `?image=<image file name>` statement. This statement must be placed on a separate line.

Full paths to all images referenced in the form's source code must be [provided](/omr/java/generate-template/#adding-images) to the template generator.

{{% alert color="primary" %}} 
Check the size and proportions of the image before adding it to the form. Very large images may break the layout.
{{% /alert %}}

### Attributes

The **image** element can be customized by adding optional attributes to it.

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?image=` statement or another attribute, and must begin with a **tab character**.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**width** | Original image width | Image width, in pixels. Smaller or larger images will be resized. | `width=640`
**height** | Original image height | Image height, in pixels. Smaller or larger images will be resized. | `height=480`
**x** | n/a | Set the absolute position of the image relative to the left edge of the page. | `x=300`
**y** | n/a | Set the absolute position of the image relative to the top edge of the page. | `y=500`

## **Example**

```
?image=logo.png
	x=200
	y=150
	width=400
	height=400
?text=Aspose.OMR for Java
	font_size=24
```

![Image](image.png)
