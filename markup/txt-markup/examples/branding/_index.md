---
weight: 30
date: "2023-05-30"
author: "Vladimir Lapin"
type: docs
url: /txt-markup/examples/branded-survey/
aliases:
- /net/txt-markup/examples/branded-survey/
feedback: OMRCOMMON
title: Branded survey
description: A customer satisfaction survey decorated with your logo.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- image
- logo
- survey
---

In this example, we'll show the source code for a customer satisfaction survey decorated with your logo.

![Aspose logo](aspose-logo.png)

## Used elements

- [**checkbox**](/omr/txt-markup/checkbox/)  
  Generate a list of answers with blank bubbles that can accommodate any kind of marks.
- [**empty_line**](/omr/txt-markup/empty_line/)  
  Add a vertical spacing between elements.
- [**image**](/omr/txt-markup/image/)  
  Insert a picture.
- [**Question**](/omr/txt-markup/choicebox/)  
  Generate a question with a fixed number of answers.
- [**text**](/omr/txt-markup/text/)  
  Add one or more lines of text to the form.

## Source code

Adding images to a survey requires changes to both the application code and the template source.

### Application code

You must add all images you mention in the template to the global page settings when generating a printable form.

## Template source

```
?image=aspose-logo.png
	align=center
?text=Customer Satisfaction Survey
	align=center
	font_size=16
	font_style=bold
?empty_line=
#Considering your complete experience with us, how likely would you be to recommend
Aspose.OMR to a friend or colleague (a higher number means more likely)?
	(5) (4) (3) (2) (1)
#You are most satisfied with the following (select all that applies):
	() Product quality () Features () Ease of use
	() Customer support availability () Technical documentation
#How would you describe our product (select all that applies)?
	() Reliable () High quality () Unique () Useful
	() Value for money () User friendly () Complicated
#How often have you had any issues with our product/service?
	() Never () Rarely () Sometimes () Very often
#Are you considering evaluating other Aspose products?
	(Yes) Yes (No) No
?empty_line=
?checkbox=I consent to the processing of the survey data:
	bubble_size=extrasmall
	font_size=10
	threshold=15
?content=Agree
	font_size=10
&checkbox
```

## Printable form

![Printable form](survey-brand-template.png)

## Filled form

![Filled form](survey-brand-fill.png)

## Recognition results

```
Element Name,Value,
I consent to the processing of the survey data:,"Agree"
Question1,"5"
Question2,"A,C,D,E"
Question3,"B,D,E"
Question4,"B"
Question5,"Y"
```
