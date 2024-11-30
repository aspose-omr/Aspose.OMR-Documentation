---
weight: 40
date: "2024-11-29"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/
feedback: OMRNET
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
Make sure that all 5 [reference point markers](/omr/net/omr-form-structure/) are present on the image.
{{% /alert %}} 

## Initializing the recognition engine

Aspose.OMR recognition engine is initialized with the recognition pattern (a file with _.OMR_ extension), [generated](/omr/net/generate-template/) along with the printable form. The recognition pattern is loaded using `GetTemplateProcessor` method of [`Aspose.OMR.Api.OmrEngine`](https://reference.aspose.com/omr/net/aspose.omr.api/omrengine/) class:

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

## Completed form sources

Aspose.OCR for .NET can [recognize](/net/recognition/) completed interactive machine-readable PDF forms along with scanned or photographed hand-filled forms. You can provide a mix of scanned and interactive forms and get the identical [recognition results](/net/recognition/save/) regardless of the source file type.

If Aspose.OCR for .NET detects at least one interactive element (such as a checkbox or input field) in the provided PDF, it classifies the PDF as interactive and reads the built-in form elements to retrieve results. If no interactive elements are found, the form is treated as a scanned document, and filled-in elements are identified using optical mark recognition algorithms. Barcodes and QR codes are always treated as images, regardless of the PDF type.

{{% alert color="primary" %}}
The original form must be generated with Aspose.OCR for .NET 24.11.0 or later. PDF forms or images based on other sources (including earlier versions of Aspose.OMR) will be ignored.
{{% /alert %}}

## Recognizing OMR form from a single respondent

{{% alert color="primary" %}} 
The process below assumes that you are recognizing a completed form (single-page or multi-page) from a single respondent. To recognize forms from multiple respondents, use [bulk recognition](#bulk-recognition).
{{% /alert %}} 

To recognize a completed form, process its scan or photo through `Recognize` method of the [initialized](#initializing-the-recognition-engine) recognition engine. You can supply a form as:

- An absolute or relative path to the image (for single-page forms).
- An absolute or relative path to the scanned PDF (for single-page or multi-page forms).
- An absolute or relative path to the interactive PDF (for single-page or multi-page forms).
- A memory stream containing a scan or a photo of the form in any of the [supported formats](/omr/net/supported-file-formats/). Useful for building web applications or APIs.
- An array of paths to scanned form pages (for multi-page forms).
- An array of memory streams containing scans or photographs of the completed form pages in any of the [supported formats](/omr/net/supported-file-formats/). Useful for building web applications or APIs.

{{% alert color="caution" %}} 
If you provide images/PDFs without [page identifier](/omr/net/omr-form-structure/) when recognizing a multi-page form, the recognition will fail with an exception _"QR code for multi page template is not found."_.
{{% /alert %}} 

Regardless of the completed form format, the recognition method supports [accuracy adjustments](/omr/net/recognition/accuracy-threshold/) for reliable results under various conditions.

{{< tabs tabID="1" tabTotal="2" tabName1="Recognize form from file" tabName2="Recognize form from memory stream" >}}
{{< tab tabNum="1" >}}
```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("form-20230629.pdf");
```
{{< /tab >}}
{{< tab tabNum="2" >}}
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
	recognitionResult = templateProcessor.Recognize(formStream);
}
```
{{< /tab >}}
{{< /tabs >}}

## Bulk recognition

The whole idea behind OMR is to automatically process hundreds of forms. Aspose.OMR for .NET greatly simplifies this task by allowing you to recognize a directory with form images using a [single method](https://reference.aspose.com/omr/net/aspose.omr.api/templateprocessor/recognizefolder/) rather than recognizing files one by one:

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResults[] = templateProcessor.RecognizeFolder(@"C:\final_exam\");
```

## Saving recognition results

Recognition results are returned in the most popular data storage formats that can be imported into any popular database or analysis system: CSV, XML or JSON. See more information in the [dedicated article](/omr/net/recognition/save/).

## Interactive adjustments and debugging

You can use the [graphical user interface control](/omr/net/working-with-ui-control/) bundled with Aspose.OMR for .NET package to interactively [fine tuning recognition accuracy](/omr/net/recognition/accuracy-threshold/) before batch processing a large number of scanned forms or for investigating recognition problems.
