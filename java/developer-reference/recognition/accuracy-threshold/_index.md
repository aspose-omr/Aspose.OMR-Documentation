---
weight: 10
date: "2022-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/recognition/accuracy-threshold/
feedback: OMRJAVA
title: Fine-tuning recognition accuracy
description: How to adjust the recognition accuracy to get reliable results for all types of marks under various conditions.
keywords:
- OMR
- recognition
- accuracy
- reliability
- threshold
- pen
- pencil
- marker
---

Different types of machine-readable forms can take different types of marks. Answer sheets usually require the bubbles to be completely filled with a pen or marker. Ballot boxes are typically marked with checkmarks or crosses. Surveys and questionnaires are sometimes filled with a pencil so that corrections can be made. In addition, paper quality, watermarks, and even lighting conditions when photographing a completed form can adversely affect recognition accuracy.

All Aspose.OMR for Java [recognition methods](/omr/java/recognition/) support `recognitionThreshold` parameter that allows you to fine-tune form processing and produce results with near 100% accuracy. This parameter is called **recognition accuracy threshold**.

From a technical standpoint, it defines the fill percentage of the bubble from `0` (empty bubble) to `100` (completely filled bubble). Lower values allow even the lightest marks (such as pencil dots or crosses) to be recognized, but may cause dirt, paper defects, or watermarks to be identified as false positives. Higher values require a more solid fill and may cause pencil marks or small checkmarks to be ignored.

![Recognition accuracy threshold](recognitionThreshold.png)

{{% alert color="primary" %}} 
It is very important that all the bubbles in the form are filled in the same manner by all respondents. Otherwise, the recognition results in batch processing may be unreliable, regardless of the threshold value.
{{% /alert %}} 

## Hints

- Increase the recognition accuracy threshold if the paper you are printing forms on has security watermarks, such as ballots or answer sheets. Otherwise, watermarks within bubbles may be considered as choices.
- It is not recommended to set the recognition accuracy threshold to values higher than `70`. This would require almost the entire bubble to be completely filled with a dark pen, which can be a burden on respondents.
- The automatic recognition threshold (if the `recognitionThreshold` parameter is omitted) depends on the bubble type and provides reliable results in most use cases.

## Example

```java
OmrEngine engine = new OmrEngine();
TemplateProcessor processor = engine.getTemplateProcessor("pattern.omr");
RecognitionResult result = processor.recognizeImage("survey123.png", 35);
String csv = result.getCsv();
System.out.println(csv);
```
