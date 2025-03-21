---
weight: 30
date: "2025-03-20"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-forms/verticalchoiceboxconfig/
feedback: OMRNET
title: VerticalChoiceBoxConfig
description: VerticalChoiceBoxConfig element generates a vertical question block with multiple answers and an optional write-in field.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
- question
- open
- vertical
- write-in
---

This element generates a vertical block with answers. 

**VerticalChoiceBoxConfig** also supports [**WriteInConfig**](/omr/net/programmatic-forms/writeinconfig/) element that allows for implementing open-ended questions.

## Declaration

**VerticalChoiceBoxConfig** element is declared as an instance of [`VerticalChoiceBoxConfig`](https://reference.aspose.com/omr/net/aspose.omr.generation.config.elements.parents/verticalchoiceboxconfig/) class. Reference `Aspose.OMR.Generation.Config.Elements.Parents`, `Aspose.OMR.Generation.Config.Elements` and `Aspose.OMR.Generation.Config.Enums` namespaces to use `VerticalChoiceBoxConfig` types without specifying the fully qualified namespace:

```csharp
using Aspose.OMR.Generation.Config.Elements;
using Aspose.OMR.Generation.Config.Elements.Parents;
using Aspose.OMR.Generation.Config.Enums;
```

The question text / label is specified in the **Name** property.

Answers are provided as a list of [**AnswerConfig**]({{< ref "#answerconfig-element" >}}) objects in the **Children** property.

```csharp
new VerticalChoiceBoxConfig() {
	Children = new List<BaseConfig>() {
		/*
		 * Put one or more AnswerConfig elements here
		 */
	}
}
```

{{% alert color="primary" %}} 

**VerticalChoiceBoxConfig** elements can only be nested within [BlockConfig](/omr/net/programmatic-forms/blockconfig/) elements and cannot be used at the top level of the form hierarchy.

{{% /alert %}}

### Required properties

Name | Type | Description
---- | ---- | -----------
**Children** | `List<BaseConfig>` | A list of [**AnswerConfig**]({{< ref "#answerconfig-element" >}}) objects representing the answers.

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**Name** | `string` | _n/a_ | Used as an element's identifier in recognition results and as a reminder of the element's purpose in template source; for example, `"Preference"`.<br />This text is not displayed on the form.
**Threshold** | `int` | 45 | Set the recognition accuracy for the answer bubbles, from 0 to 100. Lower values allow even the lightest marks to be recognized, but may cause dirt or paper defects to be treated as marks. Higher values require a more solid fill and may cause pencil marks or small checks to be ignored.<br /><br />![VerticalChoicebox threshold](program-threshold.png)
**TopPadding** | `int` | 0 | The vertical spacing (in pixels) before the first [**AnswerConfig**]({{< ref "#answerconfig-element" >}}) element.
**BubblePosition** | `string` | The bubble position relative to the answer text:<ul><li>`"left"`</li><li>`"right"`</li></ul>
**BubbleType** | `string` | The bubble design:<ul><li>`"round"` - oval;</li><li>`"square"` - box.</li></ul>

### AnswerConfig element

This element declares an answer to the **VerticalChoiceBoxConfig** question.

**AnswerConfig** element is declared as an instance of [`AnswerConfig`](https://reference.aspose.com/omr/net/aspose.omr.generation.config.elements.parents/answerconfig/) class.

Each **AnswerConfig** element can include the following elements (as well as their combinations) in its **children** property:

- [**ParagraphConfig**](/omr/net/programmatic-forms/paragraphconfig/)
- [**ContentConfig**](/omr/net/programmatic-forms/contentconfig/)
- [**WriteInConfig**](/omr/net/programmatic-forms/writeinconfig/)

#### Required properties

Name | Type | Description
---- | ---- | -----------
**children** | `List<BaseConfig>()` | A list of [**ParagraphConfig**](/omr/net/programmatic-forms/paragraphconfig/), [**ContentConfig**](/omr/net/programmatic-forms/contentconfig/), or [**WriteInConfig**](/omr/net/programmatic-forms/writeinconfig/) elements that form the answer text.

#### Optional properties

{{% alert color="primary" %}} 
These properties can override the settings of the entire **VerticalChoiceBoxConfig** element.
{{% /alert %}}

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**Name** | `string` | _n/a_ | Used for identifying the marked answer in recognition results.
**BubblePosition** | `string` | _auto_ | Override the bubble position relative to the answer text:<ul><li>`"left"`</li><li>`"right"`</li></ul> By default, the button position depends on the selected writing system (LTR or RTL).
**BubbleType** | `string` | `"round"` | Override the bubble design:<ul><li>`"round"` - oval;</li><li>`"square"` - box.</li></ul>
**Selectable** | `bool` | true | Whether to display the bubble for the answer.<br />**Setting this attribute to `false` removes the bubble in the generated form. This results in the answer cannot be chosen by the respondents.**
**BubbleOffsetX** | `int` | _auto_ | Bubble offset relative to the left (for LTR layouts) or right (for RTL layouts) of the **answer** element.<br />By default, the bubble is positioned to the left (for LTR layouts) or to the right (for RTL layouts) of the **answer** element.
**BubbleOffsetY** | `int` | _auto_ | Bubble offset, relative to the top of the **answer** element.<br />By default, the bubble is centered along the cross-axis of the first line of the **answer** element.

## Combining with WriteInConfig elements

The **AnswerConfig** element may contain a [**WriteInConfig**](/omr/net/programmatic-forms/writeinconfig/) element to allow respondents to provide free-form answers to an open-ended question. You can add several write-in fields per **VerticalChoiceBoxConfig** element.

If the bubble is marked, the contents of the corresponding **WriteInConfig** element are saved to [Images](https://reference.aspose.com/omr/net/aspose.omr.model/recognitionresult/properties/images) collection. It will work even if the [`Required`](/omr/net/programmatic-forms/writeinconfig/#optional-properties) property of the **WriteInConfig** is set to `false`.

{{% alert color="primary" %}}
Each **WriteInConfig** element must have a unique name.
{{% /alert %}}

## Example

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				new ContainerConfig() {
					Children= new List<BaseConfig>() {
						new BlockConfig() {
							BorderType = BorderType.Square,
							BorderSize = 5,
							Children = new List<BaseConfig>() {
								new ContentConfig() {
									Name = "What does OMR stand for?",
									FontSize = 12,
									FontStyle = FontStyle.Bold
								},
								new VerticalChoiceBoxConfig() {
									Name = "Definition",
									TopPadding = 100,
									Children = new List<BaseConfig>() {
										new AnswerConfig() {
											Name = "1",
											Children = new List<BaseConfig>() {
												new ContentConfig {
													Name = "Optical mark recognition",
													FontSize = 10,
													FontStyle = FontStyle.Bold
												}
											}
										},
										new AnswerConfig() {
											Name = "2",
											Children = new List<BaseConfig>() {
												new ContentConfig {
													Name = "Optical character recognition",
													FontSize = 10,
													FontStyle = FontStyle.Bold
												}
											}
										},
										new AnswerConfig() {
											Name = "3",
											Children = new List<BaseConfig>() {
												new ContentConfig {
													Name = "Own answer",
													FontSize = 10,
													FontStyle = FontStyle.Bold
												},
												new WriteInConfig() {
													Name = "Own answer"
												}
											}
										}
									}
								}
							}
						}
					}
				}
			}
		}
	}
};
```

![vertical_choicebox example](vertical_choicebox-example.png)
