---
weight: 20
date: "2023-06-29"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/save/
feedback: OMRNET
title: Saving recognition results
description: How to get form recognition results in CSV, XML or JSON formats.
keywords:
- OMR
- recognition
- save
- table
- database
- SQL
- NoSQL
- Elasticsearch
- analytics
---

After the [recognition](/omr/net/recognition/) is finished, you can get results in the most popular data storage formats.

## Saving as CSV

**Comma-separated values (CSV)** is a lightweight text format that uses a comma to separate values in a table-like structure. Best suited for spreadsheet applications and simple relational database tables.

To get recognition results in CSV format, use the following methods of [`Aspose.OMR.Model.RecognitionResult`](https://reference.aspose.com/omr/net/aspose.omr.model/recognitionresult/) class:

### GetCsv

Returns a string with the recognition results in CSV format. You can optionally specify the encoding (default is _UTF-8_).

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
string result = recognitionResult.GetCsv();
```

### GetCsvAsStream

Returns a `MemoryStream` object in the specified encoding with the recognition results in CSV format.

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
MemoryStream result = recognitionResult.GetCsvAsStream(Encoding.UTF8);
```

## Saving as JSON

**JSON** is the most popular popular open standard format for describing nested data structures. Best suited for NoSQL databases or web.

To get recognition results in JSON format, use the following methods of [`Aspose.OMR.Model.RecognitionResult`](https://reference.aspose.com/omr/net/aspose.omr.model/recognitionresult/) class:

### GetJson

Returns a string with the recognition results in JSON format. You can optionally specify the encoding (default is _UTF-8_).

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
string result = recognitionResult.GetJson();
```

### GetJsonAsStream

Returns a `MemoryStream` object in the specified encoding with the recognition results in JSON format.

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
MemoryStream result = recognitionResult.GetJsonAsStream(Encoding.UTF8);
```

## Saving as XML

**Etensible Markup Language (XML)** is a universal format for most systems - from databases to CRM.

To get recognition results in XML format, use the following methods of [`Aspose.OMR.Model.RecognitionResult`](https://reference.aspose.com/omr/net/aspose.omr.model/recognitionresult/) class:

### GetXml

Returns a string with the recognition results in XML format. You can optionally specify the encoding (default is _UTF-8_).

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
string result = recognitionResult.GetXml();
```

### GetXmlAsStream

Returns a `MemoryStream` object in the specified encoding with the recognition results in XML format.

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Api.TemplateProcessor templateProcessor = omrEngine.GetTemplateProcessor("pattern.omr");
Aspose.OMR.Model.RecognitionResult recognitionResult = templateProcessor.Recognize("filled-form.png");
MemoryStream result = recognitionResult.GetXmlAsStream(Encoding.UTF8);
```
