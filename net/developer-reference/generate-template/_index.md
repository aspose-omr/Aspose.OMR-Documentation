---
weight: 30
date: "2022-04-19"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/
title: Generating the template
description: 
keywords:
- render
- page
- form
- print
- paper
- pattern
---

{{% alert color="primary" %}} 

Try online! You can test Answer Sheet generator online at https://products.aspose.app/omr/create-answer-sheet

{{% /alert %}}

## Text markup

To create template you can pass path to a file with [text markup](/omr/net/txt-markup/).

### AnswerSheet.txt content
```text
?answer_sheet=Questions
	elements_count=100
```
### C# code
```csharp
public static void CreateAnswerSheet()
{
    // path to the txt file with Template Markup
    string markupPath = @"AnswerSheet.txt";

    // path to the output folder, where generated image and omr file will be placed 
    string outputPath = @"MyTemplates\AnswerSheet\";
    
    // name of the generated image and omr file
    string resultName = "SimpleAnswerSheet";

    OmrEngine engine = new OmrEngine();
    GenerationResult res = engine.GenerateTemplate(markupPath);
    res.Save(outputPath, resultName);
}
```

## JSON markup

To create template you can pass path to a file with [JSON markup](/omr/net/json-markup/).

### AnswerSheet.json content
```json
{
	"element_type": "Template",
	"children": [{
		"element_type": "Page",
		"children": [{
			"element_type": "AnswerSheet",
			"elements_count": 100
		}]
	}]
}
```
### C# code
```csharp
public static void CreateAnswerSheet()
{
    // path to the json file with Template Markup
    string markupPath = @"AnswerSheet.json";

    // path to the output folder, where generated image and omr file will be placed 
    string outputPath = @"MyTemplates\AnswerSheet\";
    
    // name of the generated image and omr file
    string resultName = "SimpleAnswerSheet";

    OmrEngine engine = new OmrEngine();
    GenerationResult res = engine.GenerateJSONTemplate(markupPath);
    res.Save(outputPath, resultName);
}
```
