---
weight: 40
date: "2022-04-29"
author: "Vladimir Lapin"
type: docs
url: /net/json-markup/scoregroup/
feedback: OMRNET
aliases:
- /net/template-generation/json/elements-description/score/
title: ScoreGroup
description: ScoreGroup element defines a group of questions with multiple evaluation criteria, which are summed up during recognition.
keywords:
- layout
- markup
- template
- design
- form
- JSON
- survey
- score
- total
- sum
---

This element defines a group of questions with multiple evaluation criteria. The marked criteria for each question are summarized upon recognition and the resulting value is used as an answer for the question.

**Score_group** content is organized in a tabular view for better readability.

## Declaration

This element is declared as an object with `"element_type": "ScoreGroup"` property.

Questions are provided as an array of [**ScoreQuestion**]({{< ref "#scorequestion-element" >}}) objects in the **children** property.

```json
{
	"element_type": "ScoreGroup",
	"children": [
		/*** put one or more ScoreQuestion elements here */
	]
}
```

![ScoreGroup structure](json-scoregroup.png)

### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"ScoreGroup"` (case-insensitive).
**children** | array | An array of [**ScoreQuestion**]({{< ref "#scorequestion-element" >}}) objects representing the questions.

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**name** | string | _n/a_ | Used as an element's identifier and as a reminder of the element's purpose in template source; for example, `"Satisfaction survey"`.<br />This text is not displayed on the form.
**score_type_table** | string | "table" | Layout of the **ScoreGroup** element.<br />This property is reserved for future use.

### ScoreQuestion element

This element defines the question to be rated based on the underlying criteria.

The element is declared as an object with `"element_type": "ScoreQuestion"` property.

Question text is provided in the **name** property.

Criteria, bubbles and custom content for the question are organized in a tabular view. The number of columns and their relative proportions are provided in **row_proportions** property.

**ScoreQuestion** element includes [**ScoreHeader**]({{< ref "#scoreheader-element" >}}), [**ScoreAnswer**]({{< ref "#scoreanswer-element" >}}), and optional [**TableContent**]({{< ref "#tablecontent-element" >}}) objects in the **children** property.

```json
{
	"element_type": "ScoreQuestion",
	"name": "Question",
	"row_proportions": [80,10,10],
	"children": [
		/*** put table structure and criteria elements here */
	]
}
```

#### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"ScoreQuestion"` (case-insensitive).
**name** | string | Question text.
**row_proportions** | array | Criteria, bubbles and custom content for the question are organized in a tabular view. This property specifies the number of columns and their relative proportions.<br />The number of columns is determined by the length of the array. Column widths (in percent) are provided as array items. The grand total of all column widths must not exceed 100%.
**children** | array | An array of [**ScoreHeader**]({{< ref "#scoreheader-element" >}}), [**ScoreAnswer**]({{< ref "#scoreanswer-element" >}}), and optional [**TableContent**]({{< ref "#tablecontent-element" >}}) elements representing the criteria structure.

#### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**score_display** | string | "DontDisplay" | Defines how to display the numeric score for each evaluation criterion (value of the **score** property of [**ScoreAnswer**]({{< ref "#scoreanswer-element" >}}) element):<ul><li>`"DontDisplay"` - do not show scores;</li><li>`"DisplayInsideCell"` - show scores inside bubbles;</li><li>`"DisplayAsExtraColumn"` - show scores in an additional column. This mode requires a dedicated column to be defined in **row_proportions** property and the corresponding [**ScoreHeader**]({{< ref "#scoreheader-element" >}}) element for that column.</li></ul>
**font_family** | string | "Segoe UI" | The font family for the question text.
**font_style** | string | "regular" | The font style for the question text: `"bold"`, `"italic"` or `"underline"`.<br />Several font styles can be combined by providing them as an array, for example `["bold", "italic"]`.
**font_size** | integer | 12 | Font size for the question text.

#### ScoreHeader element

This element defines the text that will be displayed in the header cell of the corresponding column and determines the content of that column.

{{% alert color="primary" %}} 

The total number of **ScoreHeader** elements must be 1 less than the number of columns defined in the **row_proportions** property of the parent [**ScoreQuestion**]({{< ref "#scorequestion-element" >}}) element.

One column is always reserved for the [criteria text]({{< ref "#scoreanswer-element" >}}).

{{% /alert %}}

The element is declared as an object with `"element_type": "ScoreHeader"` property.

Column header text is provided in the **name** property.

The **header_type** property determines what will be displayed inside the corresponding column (see property description for details).

```json
{
	"element_type": "ScoreHeader",
	"name": "Yes",
	"header_type": "positive"
}
```

##### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"ScoreHeader"` (case-insensitive).
**name** | string | Column header text.
**header_type** | string | Determines what will be displayed inside the corresponding column. This property can take one of the following values:<ul><li>`"positive"` (default) - draw a bubble that, if marked, will add the criteria score to the resulting score of the question.</li><li>`"negative"` - draw a bubble that, if marked, will be ignored.</li><li>`"amount"` - show the criterion score in the corresponding column. Requires **score_display** property of the parent [**ScoreQuestion**]({{< ref "#scorequestion-element" >}}) element to be set to `"DisplayAsExtraColumn"`.</li><li>`"question"` - moves the first column with criteria to this position. All other columns are shifted to the left.</li><li>`"content"` - fills the column with the value of [**TableContent**]({{< ref "#tablecontent-element" >}}) element.</li></ul>

##### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**font_family** | string | "Segoe UI" | The font family for the column header text.
**font_style** | string | "regular" | The font style for the column header text: `"bold"`, `"italic"` or `"underline"`.<br />Several font styles can be combined by providing them as an array, for example `["bold", "italic"]`.
**font_size** | integer | 12 | Font size for the column header text.
**align** | string | "left" | Horizontal alignment of the column header text: `"left"`, `"center"` or `"right"`.

#### ScoreAnswer element

This element defines the evaluation criterion.

The element is declared as an object with `"element_type": "ScoreAnswer"` property.

Criterion text is provided in the **name** property.

The score (weight) of the criterion that is used for calculation is provided in the **score** property.

```json
{
	"element_type": "ScoreAnswer",
	"name": "Criterion",
	"score": 1
}
```

##### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"ScoreAnswer"` (case-insensitive).
**name** | string | Criterion text.
**score** | integer | The score (weight) of the criterion that is used for calculation.

##### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**font_family** | string | "Segoe UI" | The font family for the criterion text.
**font_style** | string | "regular" | The font style for the criterion text: `"bold"`, `"italic"` or `"underline"`.<br />Several font styles can be combined by providing them as an array, for example `["bold", "italic"]`.
**font_size** | integer | 12 | Font size for the criterion text.
**align** | string | "left" | Horizontal alignment of the criterion text: `"left"`, `"center"` or `"right"`.

#### TableContent element

This optional element allows you to define the content of the custom column declared with [**ScoreHeader**]({{< ref "#scoreheader-element" >}}) element with the **header_type** property equals to `"content"`.

The element is declared as an object with `"element_type": "TableContent"` property.

The text to be put in the custom column is provided in the **name** property.

The column and row numbers to insert the text into are provided in **column** and **row**  properties respectively.

```json
{
	"element_type": "TableContent",
	"name": "Text",
	"column": 1,
	"row": 1
}
```

##### Required properties

Name | Type | Description
---- | ---- | -----------
**element_type** | string | Must be `"TableContent"` (case-insensitive).
**name** | string | Text to be inserted at the given position.
**column** | integer | Determines the column number to insert the text into.<br />Note, that the column must be declared with [**ScoreHeader**]({{< ref "#scoreheader-element" >}}) element with the **header_type** property equals to `"content"`.
**row** | integer | Determines the row number to insert the text into.<br />This value must not exceed the number of [**ScoreAnswer**]({{< ref "#scoreanswer-element" >}}) elements!

##### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**font_family** | string | "Segoe UI" | The font family for the text.
**font_style** | string | "regular" | The font style for the text: `"bold"`, `"italic"` or `"underline"`.<br />Several font styles can be combined by providing them as an array, for example `["bold", "italic"]`.
**font_size** | integer | 12 | Font size for the text.
**align** | string | "left" | Horizontal alignment of the text: `"left"`, `"center"` or `"right"`.

## Examples

Check out the code examples to see how **ScoreGroup** elements can be used.

### Customer satisfaction survey

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Container",
					"children": [
						{
							"element_type": "ScoreGroup",
							"children": [
								{
									"element_type": "ScoreQuestion",
									"name": "How would you rate our services?",
									"row_proportions": [80, 10, 10],
									"font_style": "bold",
									"children": [
										{
											"element_type": "ScoreHeader",
											"name": "Yes",
											"header_type": "positive",
											"font_style": "bold",
											"align": "center"
										},
										{
											"element_type": "ScoreHeader",
											"name": "No",
											"header_type": "negative",
											"font_style": "bold",
											"align": "center"
										},
										{
											"element_type": "ScoreAnswer",
											"name": "The staff was friendly and helpful",
											"score": 1
										},
										{
											"element_type": "ScoreAnswer",
											"name": "The staff responded quickly",
											"score": 1
										},
										{
											"element_type": "ScoreAnswer",
											"name": "Management was available to solve problems",
											"score": 1
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

![Customer satisfaction survey with score_group](satisfaction-survey-example.png)

#### Recognition result

```
How would you rate our services?_total, "2"
Satisfaction survey_total, "2"
```

### Custom column ordering

```json
{
	"element_type": "Template",
	"children": [
		{
			"element_type": "Page",
			"children": [
				{
					"element_type": "Container",
					"children": [
						{
							"element_type": "ScoreGroup",
							"children": [
								{
									"element_type": "ScoreQuestion",
									"name": "How would you rate our services?",
									"row_proportions": [10, 10, 10, 70],
									"score_display": "DisplayAsExtraColumn",
									"font_style": "bold",
									"children": [
										{
											"element_type": "ScoreHeader",
											"name": "Score",
											"header_type": "amount",
											"font_style": "bold",
											"align": "center"
										},
										{
											"element_type": "ScoreHeader",
											"name": "Yes",
											"header_type": "positive",
											"font_style": "bold",
											"align": "center"
										},
										{
											"element_type": "ScoreHeader",
											"name": "No",
											"header_type": "negative",
											"font_style": "bold",
											"align": "center"
										},
										{
											"element_type": "ScoreHeader",
											"name": "How would you rate our services?",
											"header_type": "question"
										},
										{
											"element_type": "ScoreAnswer",
											"name": "The staff was friendly and helpful",
											"score": 1
										},
										{
											"element_type": "ScoreAnswer",
											"name": "The staff responded quickly",
											"score": 3
										},
										{
											"element_type": "ScoreAnswer",
											"name": "Management was available to solve problems",
											"score": 2
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

![Custom score_group column ordering](custom-column-ordering.png)
