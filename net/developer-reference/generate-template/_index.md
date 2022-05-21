---
weight: 30
date: "2022-04-19"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/
title: Generating the template
description: How to render a printable form and generate a recognition pattern file for Aspose.OMR engine.
keywords:
- render
- page
- form
- print
- paper
- pattern
---

To generate a printable form and a recognition pattern file, process the form's [source code](/omr/net/design-form/) with `GenerateTemplate` or `GenerateJSONTemplate` methods of [`OmrEngine` class](https://apireference.aspose.com/omr/net/aspose.omr.api/omrengine) instance.

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
```
The method depends on the template source markup.

## Text markup

Aspose.OMR [text markup](/omr/net/txt-markup/) is a lightweight markup language specifically tailored for describing content and layout of Aspose.OMR forms. It is content-focused, with minimal number of tags or formatting instructions.

You can pass the template source code to the generator in a number of ways:

### As a path to the text file

The easiest way is to call the [`GenerateTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/3) method with a relative or absolute path to the file with the source code:

```csharp
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt");
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. **Note, that if the form contains images, they will not be rendered through the basic call and you will get an error.**

Optionally, you can [customize](/omr/net/generate-template/page-setup/) the paper size, orientation, font, and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object to the [method](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/4):

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt", globalPageSettings);
```

If your form contains [images](/omr/net/txt-markup/image/) and you are fine with the default page settings, [pass](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/5) the absolute path to each image file in a string array:

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
string[] images = {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate("source.txt", images);
```

### As an array of lines

Pass all lines of the source code as a string array to the [`GenerateTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/6) method:

```csharp
string[] sourceCode = {
	"?grid=Phone number",
	"\tsections_count=7",
	"\torientation=vertical"
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate(sourceCode);
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. **Note, that if the form contains images, they will not be rendered through this call and you will get an error.**

Optionally, you can [customize](/omr/net/generate-template/page-setup/) the paper size, orientation, font, and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object to the [method](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/7):

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
globalPageSettings.ImagesPaths = new string[] {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
string[] sourceCode = {
	"?grid=Phone number",
	"\tsections_count=7",
	"\torientation=vertical"
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate(sourceCode, globalPageSettings);
```

Alternatively, you can load images used in a form from memory through a special `Aspose.OMR.Api.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`System.IO.MemoryStream`) of the image file. This parameter always takes precedence over page settings - if two images with the same file name are defined in both parameters, the one from the page settings will be ignored.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
string[] sourceCode = {
	"?grid=Phone number",
	"\tsections_count=7",
	"\torientation=vertical"
};
Aspose.OMR.Api.ImageCollection images = new Aspose.OMR.Api.ImageCollection();
images.Add("aspose-logo.png", new MemoryStream(File.ReadAllBytes(@"form\images\aspose-logo.png")));
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate(sourceCode, globalPageSettings, images);
```

### As a memory stream

Pass the source code as a MemoryStream object to the [`GenerateTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/1) method:


```csharp
Aspose.OMR.Generation.GenerationResult generationResult = null;
using(System.IO.FileStream fs = new System.IO.FileStream("source.txt", System.IO.FileMode.Open))
{
	System.IO.MemoryStream ms = new System.IO.MemoryStream();
	fs.CopyTo(ms);
	generationResult = omrEngine.GenerateTemplate(ms);
};
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. **Note, that if the form contains images, they will not be rendered through this call and you will get an error.**

Optionally, you can [customize](/omr/net/generate-template/page-setup/) the paper size, orientation, font, and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object to the [method](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatetemplate/methods/2):

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
globalPageSettings.ImagesPaths = new string[] {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
Aspose.OMR.Generation.GenerationResult generationResult = null;
using(System.IO.FileStream fs = new System.IO.FileStream("source.txt", System.IO.FileMode.Open))
{
	System.IO.MemoryStream ms = new System.IO.MemoryStream();
	fs.CopyTo(ms);
	generationResult = omrEngine.GenerateTemplate(ms, globalPageSettings);
};
```

Alternatively, you can load images used in a form from memory through a special `Aspose.OMR.Api.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`System.IO.MemoryStream`) of the image file. This parameter always takes precedence over page settings - if two images with the same file name are defined in both parameters, the one from the page settings will be ignored.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
Aspose.OMR.Api.ImageCollection images = new Aspose.OMR.Api.ImageCollection();
images.Add("aspose-logo.png", new MemoryStream(File.ReadAllBytes(@"form\images\aspose-logo.png")));
Aspose.OMR.Generation.GenerationResult generationResult = null;
using(System.IO.FileStream fs = new System.IO.FileStream("source.txt", System.IO.FileMode.Open))
{
	System.IO.MemoryStream ms = new System.IO.MemoryStream();
	fs.CopyTo(ms);
	generationResult = omrEngine.GenerateTemplate(ms, globalPageSettings, images);
};
```

## JSON markup

Aspose.OMR [JSON markup](/omr/net/json-markup/) is an easy-to-read, open standard format that supports syntax highlighting, automatic formatting, and code folding in all popular code editors.

You can pass the template source code to the generator in a number of ways:

### As a path to the JSON file

The easiest way is to call the [`GenerateJSONTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api/omrengine/methods/generatejsontemplate) method with a relative or absolute path to the file with the source code:

```csharp
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateJSONTemplate("source.json");
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. **Note, that if the form contains images, they will not be rendered through the basic call and you will get an error.**

Optionally, you can [customize](/omr/net/generate-template/page-setup/) the paper size, orientation, font, and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object to the method:

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
globalPageSettings.ImagesPaths = new string[] {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateJSONTemplate("source.json", globalPageSettings);
```

### As a string containing JSON markup data

Pass the source code as a string to the [`GenerateJSONTemplateFromString`](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatejsontemplatefromstring) method:

```csharp
string sourceCode = @"{
	""element_type"": ""Template"",
	""children"": [
		{
			""element_type"": ""Page"",
			""children"": [
				{
					""element_type"": ""Container"",
					""name"": ""Example"",
					""children"": [
						{
							""element_type"": ""Block"",
							""border"": ""square"",
							""children"": [
								{
									""element_type"": ""Content"",
									""name"": ""JSON markup example""
								}
							]
						}
					]
				}
			]
		}
	]
}";
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateJSONTemplateFromString(sourceCode);
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. **Note, that if the form contains images, they will not be rendered through this call and you will get an error.**

Optionally, you can [customize](/omr/net/generate-template/page-setup/) the paper size, orientation, font, and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object to the [`GenerateJSONTemplateFromString`](https://apireference.aspose.com/omr/net/aspose.omr.api.omrengine/generatejsontemplatefromstring) method:

```csharp
string sourceCode = @"{
	""element_type"": ""Template"",
	""children"": [
		{
			""element_type"": ""Page"",
			""children"": [
				{
					""element_type"": ""Container"",
					""name"": ""Example"",
					""children"": [
						{
							""element_type"": ""Block"",
							""border"": ""square"",
							""children"": [
								{
									""element_type"": ""Content"",
									""name"": ""JSON markup example""
								}
							]
						}
					]
				}
			]
		}
	]
}";
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
globalPageSettings.ImagesPaths = new string[] {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateJSONTemplateFromString(sourceCode, globalPageSettings);
```

Alternatively, you can load images used in a form from memory through a special `Aspose.OMR.Api.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`System.IO.MemoryStream`) of the image file. This parameter always takes precedence over page settings - if two images with the same file name are defined in both parameters, the one from the page settings will be ignored.

```csharp
string sourceCode = @"{
	""element_type"": ""Template"",
	""children"": [
		{
			""element_type"": ""Page"",
			""children"": [
				{
					""element_type"": ""Container"",
					""name"": ""Example"",
					""children"": [
						{
							""element_type"": ""Block"",
							""border"": ""square"",
							""children"": [
								{
									""element_type"": ""Content"",
									""name"": ""JSON markup example""
								}
							]
						}
					]
				}
			]
		}
	]
}";
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
Aspose.OMR.Api.ImageCollection images = new Aspose.OMR.Api.ImageCollection();
images.Add("aspose-logo.png", new MemoryStream(File.ReadAllBytes(@"form\images\aspose-logo.png")));
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateJSONTemplateFromString(sourceCode, globalPageSettings, images);
```

## Building forms programmatically

The contents of an OMR form can be described directly in the [application code](/omr/net/programmatic-layout/).

To generate a printable form, pass the corresponding [`TemplateConfig`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config/templateconfig) object to the [`GenerateJSONTemplate`](https://apireference.aspose.com/omr/net/aspose.omr.api/omrengine/methods/generatetemplate) method along with [`GlobalPageSettings`](https://apireference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object that [defines](/omr/net/generate-template/page-setup/) the paper size, orientation, font, images, and other layout settings that apply to all template pages:

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
globalPageSettings.ImagesPaths = new string[] {
	System.IO.Path.Combine(workingDirectory, "aspose-logo.png")
};
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate(templateConfig, globalPageSettings);
```

Alternatively, you can load images used in a form from memory through a special `Aspose.OMR.Api.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`System.IO.MemoryStream`) of the image file. This parameter always takes precedence over page settings - if two images with the same file name are defined in both parameters, the one from the page settings will be ignored.

```csharp
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings();
globalPageSettings.PaperSize = Aspose.OMR.Generation.PaperSize.Letter;
Aspose.OMR.Api.ImageCollection images = new Aspose.OMR.Api.ImageCollection();
images.Add("aspose-logo.png", new MemoryStream(File.ReadAllBytes(@"form\images\aspose-logo.png")));
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.GenerateTemplate(templateConfig, globalPageSettings, images);
```

## Read more

- [Page setup](/omr/net/generate-template/page-setup/) - customizing the paper size, orientation, font, images, and other layout settings of a printable form.
- [Adding images](/omr/net/generate-template/images/) - including images in Aspose.OMR forms.
- [Error handling](/omr/net/generate-template/error-handling/) - debugging and identifying errors in the source code of the Aspose.OMR template during generation.
- [Saving to file](/omr/net/generate-template/save/) - saving a generated printable form and a recognition pattern file on disk.
