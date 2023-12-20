---
weight: 20
date: "2023-12-20"
author: "Vladimir Lapin"
type: docs
url: /java/design-form/answer_sheet/
title: Answer sheet
feedback: OMRJAVA
description: A markup element that creates a numbered matrix of bubbles arranged in one or more columns.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- bubbles
- exam
- quiz
- condensed
---

This element generates a numbered matrix of bubbles onto which the answers to the supplemental assessment questions must be marked. Bubbles can be arranged in multiple columns to make more efficient use of space.

It is best suited for exam papers where you want to fit the maximum number of answers on a single page. If you want to place questions on the same sheet, use [question](/omr/java/design-form/question/) markup element.

## Syntax

The element is declared with `?answer_sheet=[name]` statement. This statement must be placed on a separate line.

`name` property is used as an element's identifier in recognition results and as a reminder of the element's purpose in template source; for example, "_Biology Quiz_". The **name** is not displayed on the form.

### Attributes

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?answer_sheet=` statement or another attribute, and must begin with a **tab character**.

#### Required

Specify the number of exam questions that the answer sheet corresponds to in the **elements_count** attribute. Each question will correspond to a numbered line with multiple answer bubbles.

For example, `elements_count=100`.

{{% alert color="primary" %}}
If you omit this attribute or set its value to `0`, **answer_sheet** element will not be rendered.
{{% /alert %}}

#### Optional

The **answer_sheet** element can be customized by adding optional attributes to it.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**columns_count** | 4 | The number of columns to arrange lines into. Use multiple columns to make the answer sheet more compact. | `columns_count=3`
**answers_count** | 4 | The total number of bubbles (answers) for each question.<br />You can only set the same number of answers for all questions. If the number of answers is different for each section of the exam, use multiple **answer_sheet** elements. | `answers_count=5`
**start_id** | Automatic | The number of the first line used as a base for further numbering.<br />If omitted, the number will be calculated based on the numbering of previous elements. | `start_id=1`
**bubble_size** | `normal` | Size of bubbles:<ul><li>`extrasmall` - 40 pixels</li><li>`small` - 50 pixels</li><li>`normal` - 60 pixels</li><li>`large` - 80 pixels</li><li>`extralarge` - 100 pixels</li></ul>Overrides the global bubble size configured in [page settings](/omr/java/generate-template/page-setup/).

## Example

```text
?text=Biology Quiz
	font_size=16
	font_style=bold
?answer_sheet=Plants
	elements_count=15
	columns_count=3
	answers_count=5
```

![answer_sheet example](answer_sheet-example.png)
