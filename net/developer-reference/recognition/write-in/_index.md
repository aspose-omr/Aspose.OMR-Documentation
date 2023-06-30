---
weight: 30
date: "2023-06-29"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/write-in/
feedback: OMRNET
title: Processing write-in fields
description: How to recognize fields in which the respondent can hand write some text or draw a picture.
keywords:
- OMR
- recognition
- write-in
- picture
---

Aspose.OMR supports [several types of fields](/omr/net/design-form/) that allow the respondent to hand write some text or draw a picture. These fields are stored in `Images<System.Drawing.Bitmap>` collection in recognition results.

![Write-in fields](write-in-recognize.png)

While Aspose.OMR does not support optical character recognition (OCR) at the moment, you can combine it with [Aspose.OCR](https://products.aspose.app/ocr) to process fields that contain hand-written text.

{{% alert color="primary" %}} 

You must add a reference to `System.Drawing` assembly to your application in order to iterate through `Images` collection and save the contents of write-in fields to disk.

{{% /alert %}} 

## Form

```
?container=Example
?block=Write-in elements
?content=Your name:
	font_style=Bold
?write_in=Full name
	required=true
?content=Your phone number:
	font_style=Bold
?write_in=Phone
	required=true
&block
&container
```

![Filled form](filled-form.png)

## Processing

```csharp
string appPath = Path.GetDirectoryName(typeof(Program).Assembly.Location);
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("form-20220519.png");
int i = 1;
foreach(System.Drawing.Bitmap bitmap in recognitionResult.Images)
{
	string writeInPath = Path.Combine(appPath, $"image{i++}.png");
	bitmap.Save(writeInPath);
}
```

## Results

**image1.png**

![Write-in: Full name](image1.png)

**image2.png**

![Write-in: Full name](image2.png)
