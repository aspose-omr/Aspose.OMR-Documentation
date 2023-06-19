---
weight: 40
date: "2023-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/recognition/
aliases:
- /java/perform-omr-on-images/
feedback: OMRJAVA
title: Optical mark recognition
description: How to recognize the completed form and get results with Aspose.OMR for Java.
keywords:
- OMR
- recognition
- scan
- photo
- digitize
- result
---

To recognize an exam sheet, survey, ballot, or other completed machine-readable form, digitize it in one of the [supported formats](/omr/java/supported-file-formats/). For best results, we recommend using a scanner (a basic office scanner or a copier will be enough). If you do not have a scanner, you can simply take a picture of the form with a smartphone.

{{% alert color="primary" %}} 
- If using a smartphone, hold it parallel to the paper and make sure the sheet is well lit with minimal glares and gradients.
- The page must cover the entire area of the photo, with all 4 [black squares](/omr/java/omr-form-structure/) in the corners present on the image.
{{% /alert %}} 

## 1. Initializing the recognition engine

Aspose.OMR for Java recognition engine is initialized with the recognition pattern (a file with _.OMR_ extension), [saved](/omr/java/generate-template/#saving-a-printable-form) along with the printable form. The recognition pattern is loaded using `getTemplateProcessor` method of [`OmrEngine`](https://reference.aspose.com/omr/java/com.aspose.omr/omrengine/) class:

```java
OmrEngine engine = new OmrEngine();
TemplateProcessor processor = engine.getTemplateProcessor("pattern.omr");
```

### Recovering a recognition pattern file

If you have lost the recognition pattern file for the completed form, simply [generate](/omr/java/generate-template/) it again from the [form's source code](/omr/java/design-form/) using **exactly the same** paper size, font, and other [layout setting](/omr/java/generate-template/page-setup/).

## 2. Recognizing OMR forms

To recognize a completed form, process its scanned image or photo through `recognizeImage` method of the [initialized]({{< ref "#initializing-the-recognition-engine" >}}) recognition engine:

```java
OmrEngine engine = new OmrEngine();
TemplateProcessor processor = engine.getTemplateProcessor("pattern.omr");
RecognitionResult result = processor.recognizeImage("survey123.png");
```

The recognition method support [accuracy adjustments](/omr/java/recognition/accuracy-threshold/) for reliable results for different types of marks under various conditions.

## 3. Saving recognition results

After the recognition is finished, you can get results in the most popular data storage formats.

### Saving as CSV

**Comma-separated values (CSV)** is a lightweight text format that uses a comma to separate values in a table-like structure. Best suited for spreadsheet applications and simple relational database tables.

To save recognition results in CSV format, call `getCsv` method of the [recognition result object](#recognizing-omr-forms):

```java
OmrEngine engine = new OmrEngine();
TemplateProcessor processor = engine.getTemplateProcessor("pattern.omr");
RecognitionResult result = processor.recognizeImage("survey123.png");
String csv = result.getCsv();
System.out.println(csv);
```

### Saving as JSON

**JSON** is the most popular popular open standard format for describing nested data structures. Best suited for NoSQL databases or web.

To save recognition results in JSON format, call `getJson` method of the [recognition result object](#recognizing-omr-forms):

```java
OmrEngine engine = new OmrEngine();
TemplateProcessor processor = engine.getTemplateProcessor("pattern.omr");
RecognitionResult result = processor.recognizeImage("survey123.png");
String csv = result.getJson();
System.out.println(csv);
```
