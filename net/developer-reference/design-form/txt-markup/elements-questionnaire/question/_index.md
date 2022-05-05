---
weight: 10
date: "2022-04-25"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/question/
title: Question
description: A simple element that generates a question with a fixed number of answers.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- survey
- question
---

This element generates a question with a fixed number of answers. The respondent picks an answer by filling in the bubble next to it or by choosing a score on the rating scale.

## Syntax

The element is declared with `#` statement immediately followed by a question text. This statement must be placed on a separate line.

### Answers

Answers are provided on new lines after the opening `#` statement and continue until an empty line or another element declaration is found. Each line must begin with a **tab character**. 

The answer is declared in the form `([character]) {Answer text}`, where `character` specifies the symbol to be placed inside the answer bubble. For example, `(α) Alpha Centauri`. The character is optional; if it is omitted, the letters A through Z will be used.

Multiple answers can be placed one after the other or on new lines starting with a **tab character**. If the answer is placed on a new line, it will be displayed on a new line in the generated form. For example:

```
	(α) Alpha Centauri (β) Beta Geminorum
	(γ) Gamma Cassiopeiae
```

![Multi-line answers](answers-example.png)

#### Rating scale

You can omit the answer text and use `([character])` syntax alone to create rating scales. For example, `(5) (4) (3) (2) (1)`.

![Rating scale](rating-scale-example.png)

## Examples

Check out the code examples to see how questions can be used.

### Closed-ended question

```
#Which Aspose.OMR features do you consider the most valuable?
	() Recognition accuracy () Wide range of supported file formats
	() Form generation () QR codes and barcodes support
```

![Closed-ended question example](closed-ended-question-example.png)

### Yes / no options

```
#Would you recommend Aspose.OMR to your colleagues?
	(Yes) Yes, sure! (No) Unlikely
```

![Yes / no options example](yes-no-example.png)

### Question with a rating scale

```
#On a scale of 5 to 1, how do you feel?
	(5)(4)(3)(2)(1)
```

![Question with a rating scale](question-with-rating-scale-example.png)
