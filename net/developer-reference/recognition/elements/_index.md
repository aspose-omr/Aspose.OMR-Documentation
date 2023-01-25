---
weight: 40
date: "2022-05-24"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/elements/
feedback: OMRNET
title: How form elements are recognized
description: How Aspose.OMR for .NET recognizes different types of elements in forms.
keywords:
- OMR
- recognition
- fields
- elements
- blocks
- result
---

Below is information and examples on how Aspose.OMR for .NET recognizes different types of elements in forms.

## WriteIn

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/write_in/)
- [JSON markup](/omr/net/json-markup/writein/)

### Mapping

The image of the **WriteIn** field is stored as `System.Drawing.Bitmap` object in `Images` collection. It does not appear in CSV / JSON / XML [recognition results](/omr/net/recognition/save/).

### Example

See [Processing write-in fields](/omr/net/recognition/write-in/) for details.

</details>

## Barcode

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/elements-barcode/)
- [JSON markup](/omr/net/json-markup/elements-barcode/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **Barcode** element.
Value | Decoded barcode.

### Example

```
Element Name,Value,
QR code,“https://products.aspose.com/omr/net/"
```

</details>

## Question (ChoiceBox)

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/question/)
- [JSON markup](/omr/net/json-markup/choicebox/)

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

</details>

## CheckBox

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/checkbox/)
- [JSON markup](/omr/net/json-markup/checkbox/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **CheckBox** element.
Value | Marked boxes, separated by commas.

### Example

```
Element Name,Value,
Food preference:,"Vegan,Low-carb"
```

</details>

## VerticalChoiceBox

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/vertical_choicebox/)
- [JSON markup](/omr/net/json-markup/verticalchoicebox/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **VerticalChoiceBox** element.
Value | Marked answers, separated by commas.

### Example

```
Element Name,Value,
Definition,"1"
```

</details>


## ScoreGroup

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/score_group/)
- [JSON markup](/omr/net/json-markup/scoregroup/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | <ul><li>For each **ScoreQuestion** element, an entry with `name` property of **ScoreQuestion** element is added.</li><li>For each **ScoreQuestion** element, an entry with `name` property of **ScoreQuestion** element and `_total` suffix is added.</li><li>For the entire **ScoreGroup** element, the entry with `name` property of **ScoreGroup** element and `_total` suffix is added.</li></ul>
Value | <ul><li>Marked evaluation criteria for each **ScoreQuestion** element, separated by commas.</li><li>Aggregated score for each **ScoreQuestion** element.</li><li>Total score for the entire **ScoreGroup** element.</li></ul>

### Example

```
Element Name,Value,
How would you rate our services?,"The staff was friendly and helpful,Management was available to solve problems"
How would you rate our services?_total,"3"
Satisfaction survey_total,"3"
```

</details>

## Table

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/table/)
- [JSON markup](/omr/net/json-markup/table/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of each **Question** element.
Value | Marked answer text.

### Example

```
Element Name,Value,
Are you satisfied with Aspose.OMR for .NET performance?,"I don't know"
Are you satisfied with Aspose.OMR for .NET recognition accuracy?,"Yes"
Is Aspose.OMR for .NET easy to use?,"Yes"
```

</details>

## Answer Sheet

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/answer_sheet/)
- [JSON markup](/omr/net/json-markup/answersheet/)

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

</details>

## Grid

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/grid/)
- [JSON markup](/omr/net/json-markup/grid/)

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

</details>

## CustomAnswerSheet

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/custom_answer_sheet/)
- [JSON markup](/omr/net/json-markup/customanswersheet/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **CustomAnswerSheet** element followed by underscore and the question number.
Value | Answer.

### Example

```
Element Name,Value,
Example_1,"A"
Example_2,"C"
Example_3,"D"
Example_4,"C"
Example_5,"B"
Example_6,"A"
Example_7,"A"
Example_8,"C"
Example_9,"D"
Example_10,"D"
Example_11,"B"
Example_12,"B"
Example_13,"A"
Example_14,"D"
Example_15,"C"
```

</details>

## CompositeGrid

<details>
<summary>Show / hide details</summary>

- [Text markup](/omr/net/txt-markup/composite_grid/)
- [JSON markup](/omr/net/json-markup/compositegrid/)

### Mapping

Recognition result | Value
------------------ | -----
Element Name | `name` property of the **CompositeGrid** element.
Value | Symbols from each marked bubble merged into a single value. If more than one bubble are marked per row / column, an error is written into the results.

### Example

```
Element Name,Value,
Security word 1,"SECRET"
Security word 2,"ERROR: Multiple marks per symbol"
```

</details>