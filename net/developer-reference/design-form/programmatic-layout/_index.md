---
weight: 30
date: "2022-04-19"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-layout/
title: Building forms programmatically
description: Describe the OMR form directly in the application code.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
---

You can describe the layout and contents of an OMR form directly in the application code.

The form is created as an instance of [TemplateConfig](https://apireference.aspose.com/omr/net/aspose.omr.generation.config/templateconfig) object.

```csharp
public static void CreateAnswerSheet()
{
	//root object TemplateConfig with all nested elements
	TemplateConfig config = new TemplateConfig();
	{
		Children = new List<BaseConfig>()
		{
			new PageConfig()
			{
				Children = new List<BaseConfig>()
				{
					new AnswerSheetConfig()
					{
						ElementsCount = 100
					}
				}
			}
		}
	};

    // path to the output folder, where generated image and omr file will be placed 
    string outputPath = @"MyTemplates\AnswerSheet\";
    
    // name of the generated image and omr file
    string resultName = "SimpleAnswerSheet";

    OmrEngine engine = new OmrEngine();
    GenerationResult res = engine.GenerateTemplate(config);
    res.Save(outputPath, resultName);
}
```

![OmrAnswerSheet](AnswerSheet.png)
