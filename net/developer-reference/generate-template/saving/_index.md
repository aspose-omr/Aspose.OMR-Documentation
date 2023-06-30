---
weight: 40
date: "2023-06-29"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/save/
feedback: OMRNET
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

- Printable form as an image or PDF document.
- A recognition pattern used by Aspose.OMR recognition engine, in a special _.OMR_ format. This file is **required** for mapping optical marks to form elements and is necessary for [recognizing](/omr/net/recognition/) filled forms!  

## Saving form to a file

The printable form can be saved in one or more images (one image per page) or in one PDF document. Regardless of the chosen format, the recognition pattern file is always saved to the save folder.

### Saving form as an image

Call `Save` method of of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/). The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory.
- File name (without extension) for printable form pages and the recognition pattern. Each page is always saved as a separate file. If multiple pages are generated, the suffix "_Page{NUMBER}_" will be added to each file; for example, "_OMR-FormPage1.png_".

Printable pages are saved as _PNG_ images. Their dimensions match the provided [paper size](/omr/net/generate-template/page-setup/#supported-paper-sizes) and orientation.

{{< tabs tabID="1" tabTotal="2" tabName1="Source code" tabName2="Saved files" >}}
{{< tab tabNum="1" >}}
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
{{< /tab >}}
{{< tab tabNum="2" >}}
- OMR-Form.png
- OMR-Form.omr
{{< /tab >}}
{{< /tabs >}}

### Saving form as a PDF document

{{% alert color="primary" %}} 
This is the recommended method for saving multi-page forms.
{{% /alert %}} 

Call `SaveAsPdf` method of of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/). The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory.
- File name (without extension) for a printable form and the recognition pattern. All pages are saved to a single PDF document.

{{< tabs tabID="2" tabTotal="2" tabName1="Source code" tabName2="Saved files" >}}
{{< tab tabNum="1" >}}
```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
generationResult.SaveAsPdf("", "OMR-Form");
```
{{< /tab >}}
{{< tab tabNum="2" >}}
- OMR-Form.pdf
- OMR-Form.omr
{{< /tab >}}
{{< /tabs >}}

## Generating form to a memory stream

If you do not have direct access to storage (for example, when building web applications), you can generate the form into memory.

{{% alert color="primary" %}} 
This approach requires that the recognition pattern be [generated separately](#getting-recognition-pattern).
{{% /alert %}} 

To enable in-memory form generation, convert the object returned by [`GenerateTemplate` or `GenerateJSONTemplate` methods](/omr/net/generate-template/) to [`MemoryGenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/memorygenerationresult/memorygenerationresult/) object:

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
Aspose.OMR.Generation.MemoryGenerationResult memoryGenerationResult = new Aspose.OMR.Generation.MemoryGenerationResult(generationResult);
```

### Getting form pages as images

Call [`GetImages`](https://reference.aspose.com/omr/net/aspose.omr.generation/memorygenerationresult/getimages/) method of the `MemoryGenerationResult` object. All pages of the OMR form are returned as a [collection](https://learn.microsoft.com/en-us/dotnet/api/system.collections.ienumerable) of `MemoryStream` objects containing bitmap images of form pages.

```csharp
IEnumerable<MemoryStream> pages = memoryGenerationResult.GetImages();
foreach(var page in pages)
{
	byte[] pageImageBytes = page.ToArray();
}
```

### Getting form as PDF document

Call [`GetPDF`](https://reference.aspose.com/omr/net/aspose.omr.generation/memorygenerationresult/getpdf/) method of the `MemoryGenerationResult` object. All pages of the OMR form are returned as a `MemoryStream` object containing a PDF document.

```csharp
MemoryStream form = memoryGenerationResult.GetPDF();
byte[] formBytes = form.ToArray();
```

### Getting recognition pattern

Call [`GetOmr`](https://reference.aspose.com/omr/net/aspose.omr.generation/memorygenerationresult/getomr/) method of the `MemoryGenerationResult` object. The recognition pattern is returned as a `MemoryStream` object.

```csharp
MemoryStream omr = memoryGenerationResult.GetOmr();
byte[] recognitionPattern = omr.ToArray();
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
