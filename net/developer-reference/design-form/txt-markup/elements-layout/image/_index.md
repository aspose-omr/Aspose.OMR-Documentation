---
weight: 60
date: "2022-04-21"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/image/
title: image
description: Image element is used to add a picture.
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

This element is used to add a picture.

## Syntax

The element is declared with `?image=<image file name>` statement. This statement must be placed on a separate line.

Full paths to all images used in the form are passed to the [template generator](/omr/net/generate-template/) using [ImagesPaths](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings/fields/imagespaths) parameter of the [global page settings](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings).

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
**x** | n/a | Set the absolute position of the image relative to the left edge of the page.<br />Overrides the value of **align** attribute. | `x=300`
**y** | n/a | Set the absolute position of the image relative to the top edge of the page. | `y=500`
**align** | left | Horizontal image alignment: `left`, `center` or `right`. | `align=center`

## Allowed child elements

None.

## **Example**

```
?image=logo.jpg
	align=center
?empty_line=
?text=Aspose.OMR for .NET
	align=center
	font_size=24
```

![Image](image.png)
