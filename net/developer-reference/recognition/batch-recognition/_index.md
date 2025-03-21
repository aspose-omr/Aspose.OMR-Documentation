---
weight: 30
date: "2025-03-19"
author: "Vladimir Lapin"
type: docs
url: /net/recognition/batch/
feedback: OMRNET
title: Saving recognition results
description: How to get form recognition results in CSV, XML or JSON formats.
keywords:
- OMR
- recognition
- save
- batch
- bulk
- multi
---

Bulk recognition of personalized OMR forms is handled through `Aspose.OMR.BatchProcessings.BatchTemplateProcessor` class. It is initialized with the recognition pattern (a file with _.DOMR_ extension), generated along with the printable forms.

`Aspose.OMR.BatchProcessings.BatchRecognitionResult` class contains the bulk recognition results and allows for saving them into different [formats](/omr/net/supported-file-formats/#recognition-results).

## Example

```csharp
// Initialize Aspose.OMR API
BatchOmrEngine batchEngine = new BatchOmrEngine();
// Initialize the recognition engine
BatchTemplateProcessor processor = batchEngine.GetTemplateProcessor("recognition_pattern.domr");
// Recognize all forms from the folder
BatchRecognitionResult results = processor.Recognize("exam\\scans");
results.SaveAsJson("results.json");
```
