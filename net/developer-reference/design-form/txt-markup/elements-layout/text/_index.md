---
weight: 30
date: "2022-04-21"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/text/
title: text
description: Text element is used to add one or more lines of text to the form.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
---

This element is used to add one or more lines of text to the form. **Text** elements _cannot be nested within other elements_ - they should always be top-level elements in the form hierarchy.

## Syntax

The element declaration begins with `?text=` statement followed by a text to be displayed on the form, and continues until an empty line, another element declaration, or an [attribute]({{< relref "#attributes" >}}) is found.

New lines following `?text=` declaration are treated as line breaks in the text.

{{% alert color="primary" %}} 

Never add a **tab character** before subsequent lines of text.

{{% /alert %}}

### Attributes

The **text** element can be customized by adding optional attributes to it.

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?text=` statement or another attribute, and must begin with a **tab character**.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**font_family** | Segoe UI | The font family for the text. | `font_family=Courier New`
**font_style** | regular | The font style for a text: `bold`, `italic` or `underline`.<br />Several font styles can be combined by listing them separated by commas. | `font_style=bold, italic`
**font_size** | 12 | Font size for the text. | `font_size=16`
**align** | left | Horizontal text alignment: `left`, `center` or `right`. | `align=center`


## Allowed child elements

None.

## **Example**

```
?text=Once upon a midnight dreary, while I pondered, weak and weary,
Over many a quaint and curious volume of forgotten lore-
While I nodded, nearly napping, suddenly there came a tapping,
As of some one gently rapping, rapping at my chamber door.
	font_family=Courier New
	font_style=bold, italic
	align=center
```

![Text](text.png)
