---
weight: 20
date: "2025-02-10"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/images/
feedback: OMRNET
title: Adding images
description: How to include images in Aspose.OMR forms.
keywords:
- render
- page
- form
- print
- generate
- image
- picture
---

Aspose.OMR allows you to customize questionnaires, answer sheets, and other forms by adding images (such as your company logo) to them. In addition to describing the element in the [source code](/omr/net/design-form/), the full path to _each_ image file must be directly passed to the [form generator](/omr/net/generate-template/).

{{% alert color="primary" %}}

If an image file is mentioned in the source code but no file path is provided, an error will be thrown and the form will not be generated.

{{% /alert %}}

Image paths can be provided with:

- A string array in [`Generate`] method.  
  It only works with text markup files and **does not** allow you to configure page settings.
- `ImagesPaths` property of [`GlobalPageSettings`](https://reference.aspose.com/omr/net/aspose.omr.generation/globalpagesettings) object. Full paths to images are provided as an array of strings.  
  This is a universal approach that works with all types of sources, and also allows you to [customize page settings](/omr/net/generate-template/page-setup/).
- `Aspose.OMR.Api.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`System.IO.MemoryStream`) of the image file.

## Example

Template source code:

```
?image=aspose-logo.png
	align=center
?text=Customer Satisfaction Survey
	align=center
	font_size=16
	font_style=bold
?image=vignette.png
	align=center
```

Generate and save the printable form, providing images by file paths:

```csharp
string workingDirectory = System.IO.Directory.GetCurrentDirectory();
Aspose.OMR.Generation.GlobalPageSettings globalPageSettings = new Aspose.OMR.Generation.GlobalPageSettings() {
	PaperSize = Aspose.OMR.Generation.PaperSize.Tabloid,
	BubbleColor= Aspose.OMR.Generation.Color.Red,
	ImagesPaths = new string[] {
		System.IO.Path.Combine(workingDirectory, "aspose-logo.png"),
		@"C:\Users\Public\Pictures\vignette.png"
	}
};
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.Generate("source.txt", globalPageSettings);
generationResult.Save("", "OMR-Form");
```

Generate and save the printable form, loading images from memory:

```csharp
string sourceCode = File.ReadAllText(@"source.txt");
var buffer = Encoding.UTF8.GetBytes(sourceCode);
ImageCollection images = new ImageCollection();
images.Add("aspose-logo.png", new MemoryStream(File.ReadAllBytes(System.IO.Path.Combine(workingDirectory, "aspose-logo.png"))));
images.Add("vignette.png", new MemoryStream(File.ReadAllBytes(@"C:\Users\Public\Pictures\vignette.png")));
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
using(MemoryStream source = new MemoryStream(buffer))
{
	Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.Generate(source, images);
	generationResult.Save("", "OMR-Form");
}
```
