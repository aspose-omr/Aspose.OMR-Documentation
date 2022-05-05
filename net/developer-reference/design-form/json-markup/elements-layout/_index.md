---
weight: 10
date: "2022-04-27"
author: "Vladimir Lapin"
type: docs
url: /net/json-markup/elements-layout/
title: Layout
description: Layout elements are used to arrange other elements and define the appearance and design of the OMR form.
keywords:
- layout
- markup
- template
- design
- form
- JSON
- elements
- content
---

Layout elements are used to arrange other elements and define the appearance and design of the OMR form. 

Layout elements themselves are not recognized by Aspose.OMR; however, they may contain elements that are recognized.

## Default arrangement of elements

All form elements are rendered one below the other and occupy the entire width of the **page** or the **parent element**.

![Default arrangement of elements](default-layout.png)

## Layout elements

The type of the element is specified in the value of **element_type** property of a corresponding object. The property value is provided as a case-insensitive string.

- [Container](/omr/net/json-markup/container/)  
  This element is used to break content into columns and to add a footer to the form.
- [Block](/omr/net/json-markup/block/)  
  This element is used to organize other elements in container columns.
- [Text](/omr/net/json-markup/text/)  
  This element is used to add one or more lines of text to the form. Can only be used at the **top level** of the form hierarchy.
- [Content](/omr/net/json-markup/content/)  
  This element is used to add a line of text to the parent element. Can only be used inside **other elements**.
- [EmptyLine](/omr/net/json-markup/emptyline/)  
  This element is used to add vertical spacing between elements.
- [Image](/omr/net/json-markup/image/)  
  This element is used to add a picture.
- [Paragraph](/omr/net/json-markup/paragraph/)  
  This element is used to combine text and images.
- [InputGroup](/omr/net/json-markup/inputgroup/)  
  This element is used to insert personalized information, such as the respondent's name or email, into the form.
