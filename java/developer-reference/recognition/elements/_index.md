---
weight: 20
date: "2023-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/recognition/elements/
feedback: OMRJAVA
title: How form elements are recognized
description: How Aspose.OMR for Java recognizes different types of elements in forms.
keywords:
- OMR
- recognition
- fields
- elements
- blocks
- result
---

Below is information and examples on how Aspose.OMR for Java recognizes different types of elements in forms.

## Question

[Markup language element](/omr/java/design-form/question/).

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `Question{number}`
Value | Marked bubbles, separated by commas.

### Example

```
Element Name,Value,
Question1,"A,C"
```

## Answer Sheet

[Markup language element](/omr/java/design-form/answer_sheet/).

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of each **Question** element followed by the question number.
Value | Answer.

### Example

```
Element Name,Value,
Exam1,"C"
Exam2,"A"
Exam3,"D"
Exam4,"E"
Exam5,"B"
Exam6,"B"
Exam7,"B"
Exam8,"E"
Exam9,"A"
Exam10,"C"
Exam11,"D"
Exam12,"B"
Exam13,"D"
Exam14,"E"
Exam15,"A"
```

## Grid

[Markup language element](/omr/java/design-form/grid/).

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **Grid** element.
Value | Numbers from each marked bubble merged into a single number. If more than one bubble is marked per row / column, all marked numbers are merged into the result.

### Example

```
Element Name,Value,
Phone number,"1234567"
```
