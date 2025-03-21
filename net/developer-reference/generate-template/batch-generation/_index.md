---
weight: 50
date: "2025-03-17"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/batch/
feedback: OMRNET
title: Batch generation
description: How to generate multiple personalized OMR forms.
keywords:
- render
- page
- form
- batch
- bulk
- multi
---

Aspose.OMR for .NET can automatically generate multiple personalized OMR forms, for example exam sheets for individual students. Bulk-generation is available through `Aspose.OMR.BatchProcessings.BatchOmrEngine` API.

Personalized values used for bulk form generation is provided through `Aspose.OMR.BatchProcessings.DataSet` collection. The number of generated forms is equal to the number of `Aspose.OMR.BatchProcessings.DataRecord` entries in the instance of `Aspose.OMR.BatchProcessings.DataSet` class:

```csharp
var dataSet = new DataSet();
// Add first student
var record1 = new DataRecord("JohnDoe");
record1.Fields.Add("student_name", "John Doe");
dataSet.Records.Add(record1);
// Add first student
var record2 = new DataRecord("JohnDoe");
record2.Fields.Add("student_name", "Jane Doe");
dataSet.Records.Add(record2);
```

Use `${value ID}` placeholder in [text](/net/omr/txt-markup/) or [JSON](/net/omr/json-markup/) markup to insert the field with the given ID from the `DataRecord` element into the designated position in the form:

```
?text=${student_name}
	font_style=bold
?empty_line=
?answer_sheet=Answers
	columns_count=3
	elements_count=15
	answers_count=5
```

There are two ways to bulk-generate forms. The easiest one is to use the `Generate` method of `BatchOmrEngine` class. This approach is recommended for generating a small number of forms (less than 100):

```csharp
// Initialize Aspose.OMR API
BatchOmrEngine batchEngine = new BatchOmrEngine();
// Define the type, size and position of the form identifier barcode
GlobalPageSettings settings = new GlobalPageSettings();
BarcodeConfig batchBarcode = new BarcodeConfig();
batchBarcode.BarcodeType = BarcodeType.QR;
batchBarcode.X = 500;
batchBarcode.Y = 500;
settings.BatchBarcode = batchBarcode;
// Bulk generate forms
BatchGenerationResult generationResult = batchEngine.Generate(dataSet, "source.txt", settings);
generationResult.Save("generated-templates", "recognition_pattern.domr");
```

The saved results consist of several files:

- Printable forms as images or PDF documents.
- A recognition pattern used by Aspose.OMR recognition engine, in a special _.DOMR_ format. This file is **required** for mapping optical marks to form elements and is necessary for [recognizing](/omr/net/recognition/batch/) filled forms!  

If you want to generate a very large number of forms, it is recommended to use `Aspose.OMR.BatchProcessings.TemplateExporter` class which handles advanced bulk generation and allows to iterate through generated form pages:

```csharp
// Initialize Aspose.OMR API
BatchOmrEngine batchEngine = new BatchOmrEngine();
// Define the type, size and position of the form identifier barcode
GlobalPageSettings settings = new GlobalPageSettings();
BarcodeConfig batchBarcode = new BarcodeConfig();
batchBarcode.BarcodeType = BarcodeType.QR;
batchBarcode.X = 500;
batchBarcode.Y = 500;
settings.BatchBarcode = batchBarcode;
// Bulk generate forms
BatchGenerationResult generationResult = batchEngine.Generate(dataSet, "source.txt", settings);
// Iterate through generated forms
FormExporter exporter = generationResult.getFormExporter();
while (exporter.MoveToNextForm())
{
	// Save a form to PDF
	using (var memoryStream = new MemoryStream())
	{
		exporter.ExportFormPdf(memoryStream);
	}
	// Save individual form pages to images
	while (exporter.MoveToNextPage())
	{		
		using (var memoryStream = new MemoryStream())
		{
			exporter.ExportPagePng(stream);
		}
	}
}
// Save recognition pattern
using (var memoryStream = new MemoryStream())
{
	exporter.ExportRecognitionPattern(memoryStream);
}
```
