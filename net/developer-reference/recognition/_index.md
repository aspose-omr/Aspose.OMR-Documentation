---
weight: 40
date: "2022-05-20"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/
title: Optical mark recognition (OMR)
description: How to recognize the filled form with Aspose.OMR for .NET.
keywords:
- OMR
- recognition
- scan
- photo
- digitize
- result
---

To recognize a filled questionnaire, answer sheet, ballot, or other OMR form, digitize it in one of the [supported formats](/omr/net/supported-file-formats/). For best results, we recommend using a scanner (a basic office scanner or multifunction copier will suffice). If you do not have a scanner, you can simply take a picture of the form with any modern smartphone and upload the photo to your computer.

{{% alert color="primary" %}} 

Make sure that all 4 [positioning markers](/omr/net/omr-form-structure/) are present on the image.

{{% /alert %}} 

## Initializing the recognition engine

Aspose.OMR recognition engine is initialized with the recognition pattern (a file with _.OMR_ extension), [generated](/omr/net/generate-template/) along with the printable form. The recognition pattern is loaded using `GetTemplateProcessor` method of [`Aspose.OMR.Api.OmrEngine`](https://apireference.aspose.com/omr/net/aspose.omr.api/omrengine/) class:

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
```

You can also load the recognition pattern as a `MemoryStream` object, which can be very useful when building web applications or APIs:

```csharp
byte[] pattern = Encoding.UTF8.GetBytes(payload);
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = null;
using(MemoryStream ms = new MemoryStream(pattern))
{
	templateProcessor = omrEngine.GetTemplateProcessor(ms, Encoding.UTF8);
}
```

### Recovering a recognition pattern file

If you have lost the recognition pattern file for the survey, simply [generate](/omr/net/generate-template/) it again from the [form source code](/omr/net/design-form/) using **exactly the same** paper size, orientation, font, and other [layout setting](/omr/net/generate-template/page-setup/).

## Recognizing OMR forms

{{% alert color="primary" %}} 

All recognition methods support [accuracy adjustments](/omr/net/recognition/accuracy-threshold/) for reliable results under various conditions.

{{% /alert %}} 

To recognize a filled form page, process its scan or photo with the [initialized]({{< ref "#initializing-the-recognition-engine" >}}) recognition engine using `RecognizeImage` method of the [`Aspose.OMR.Api.TemplateProcessor`](https://apireference.aspose.com/omr/net/aspose.omr.api/templateprocessor/) class:

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.RecognizeImage("form-20220519.png");
```

You can also provide a form image as a `MemoryStream` object, which can be very useful when building web applications or APIs:

```csharp
// Load recognition pattern and form image
byte[] pattern = Encoding.UTF8.GetBytes(payload[0]);
byte[] form = Encoding.UTF8.GetBytes(payload[1]);
// Initialize recognition engine
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = null;
using(MemoryStream patternStream = new MemoryStream(pattern))
{
	templateProcessor = omrEngine.GetTemplateProcessor(patternStream, Encoding.UTF8);
}
// Recognize
Aspose.OMR.Model.RecognitionResult recognitionResult = null;
using(MemoryStream formStream = new MemoryStream(form))
{
	recognitionResult = templateProcessor.RecognizeImage(formStream);
}
```

### Batch recognition

The whole idea behind OMR is to automatically process hundreds of forms. Aspose.OMR for .NET greatly simplifies this task by allowing you to recognize a directory with form images with a [single method](https://apireference.aspose.com/omr/net/aspose.omr.api/templateprocessor/recognizefolder/) instead recognizing files one by one:

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResults[] = templateProcessor.RecognizeFolder(@"C:\final_exam\");
```

### Recognizing multi-page forms

If a form consists of several pages, use [`RecognizeMultiPageTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api/templateprocessor/recognizemultipagetemplate/) method to recognize them as a single entity:

```csharp
string[] formPages = { "page1.png", "page2.png", "page3.png" };
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult[] = templateProcessor.RecognizeMultiPageTemplate(formPages);
```

## Saving recognition results

Recognition results are returned in the most popular data storage formats that can be imported into any popular database or analysis system: CSV, XML or JSON. See more information in the [dedicated article](/omr/net/recognition/save/).
