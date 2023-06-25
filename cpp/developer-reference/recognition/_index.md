---
weight: 40
date: "2023-06-23"
author: "Vladimir Lapin"
type: docs
url: /cpp/recognition/
feedback: OMRCPP
title: Optical mark recognition
description: How to recognize the completed form and get results with Aspose.OMR for C++.
keywords:
- OMR
- recognition
- scan
- photo
- digitize
- result
---

To read an answer sheet, test, survey, election ballot, or other completed OMR form, digitize it in one of the [supported formats](/omr/cpp/supported-file-formats/). For best results, we recommend using a flatbed scanner (a basic office scanner or a copier will be enough). If you do not have a scanner, simply take a picture of the form with a smartphone camera.

{{% alert color="primary" %}} 
- If using a smartphone, hold it parallel to the paper and make sure the sheet is well lit with minimal glares and gradients.
- The page must cover the entire area of the photo, with all 4 [black squares](/omr/cpp/omr-form-structure/) in the corners present on the image.
{{% /alert %}} 

The recognition is a 3-step process.

## 1. Initializing the recognition engine

Aspose.OMR for Java recognition engine is initialized with the recognition pattern (a file with _.OMR_ extension), [saved](/omr/cpp/generate-template/save/) along with the printable form. The recognition pattern is loaded using `GetTemplateProcessor` method:

```cpp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Api::TemplateProcessor> processor = engine->GetTemplateProcessor(u"pattern.omr");
```

### Recovering a recognition pattern file

If you have lost the recognition pattern file for the completed form, simply [generate](/omr/cpp/generate-template/) it again from the [form's source code](/omr/cpp/design-form/) using **exactly the same** paper size, font, and other [layout setting](/omr/cpp/generate-template/page-setup/).

## 2. Recognizing OMR forms

To recognize a form, process the scanned image or photo through `RecognizeImage` method of the [initialized]({{< ref "#initializing-the-recognition-engine" >}}) recognition engine:

```cpp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Api::TemplateProcessor> processor = engine->GetTemplateProcessor(u"pattern.omr");
System::SharedPtr<Model::RecognitionResult> result = processor->RecognizeImage(u"completed-form.jpg", 40);
```

The recognition method support [accuracy adjustments](/omr/cpp/recognition/accuracy-threshold/) for reliable results for different types of marks, even under difficult conditions (dirt, glare, and so on).

## 3. Saving recognition results

After the recognition is finished, you can get results in the most popular data storage formats.

### Saving as CSV

**Comma-separated values (CSV)** is a lightweight text format that uses a comma to separate values in a table-like structure. Best suited for spreadsheet applications and simple relational database tables.

To save recognition results in CSV format, call `GetCsv` method of the [recognition result object](#recognizing-omr-forms):

```cpp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Api::TemplateProcessor> processor = engine->GetTemplateProcessor(u"pattern.omr");
System::SharedPtr<Model::RecognitionResult> result = processor->RecognizeImage(u"completed-form.jpg", 40);
System::String resultCsv = result->GetCsv();
```

### Saving as JSON

**JSON** is the most popular popular open standard notation for describing nested data structures. Best suited for NoSQL databases or web.

To save recognition results in JSON format, call `GetJson` method of the [recognition result object](#recognizing-omr-forms):

```cpp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Api::TemplateProcessor> processor = engine->GetTemplateProcessor(u"pattern.omr");
System::SharedPtr<Model::RecognitionResult> result = processor->RecognizeImage(u"completed-form.jpg", 40);
System::String resultCsv = result->GetJson();
```
