---
weight: 40
date: "2022-05-13"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/save/
title: Saving a printable form and recognition pattern
description: How to save a generated printable form and a recognition pattern file on disk.
keywords:
- render
- page
- form
- print
- paper
- pattern
- save
- file
- image
- PDF
---

After the template has been successfully [generated](/omr/net/generate-template/), you can save it to disk in the preferred format.

The saved results consist of several files:

- Printable form pages as images or PDF files. Their dimensions match the [provided](/omr/net/generate-template/page-setup/) paper size and orientation.  
  Each page is always saved as a separate file. If multiple pages are generated, the suffix "_Page{NUMBER}_" will be added to each file; for example, "_OMR-FormPage1.png_".
- A recognition pattern used by Aspose.OMR recognition engine, in a special _.OMR_ format. This file is **required** for [recognizing](/omr/net/recognition/) filled forms, make sure you do not accidentally delete it!

Use one of the following methods, depending on your preferred format of the printable form:

## Save as image

Call `Save` method of of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/). The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory.
- File name mask (without extension) for printable form pages and the recognition pattern.

Printable pages are saved as _PNG_ images.

### Example

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
generationResult.Save("", "OMR-Form");
```

## Save as PDF

Call `SaveAsPdf` method of of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/). The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory.
- File name mask (without extension) for printable form pages and the recognition pattern.

Printable pages are saved as _PDF_ files.

### Example

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
generationResult.SaveAsPdf("result", "OMR-Form");
```

## Iterating through pages

[GenerationResult](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/) also contains a collection of all generated printable pages (as `System.Drawing.Bitmap` objects). You can manually iterate through this list and save the pages in [different formats](/omr/net/supported-file-formats/) if necessary.

### Example

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
int i = 1;
foreach(System.Drawing.Bitmap bitmap in generationResult.MultipageTemplateImages)
{
	bitmap.Save($"page-{i++}.bmp");
}
```
