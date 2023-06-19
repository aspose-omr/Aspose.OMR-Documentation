---
weight: 30
date: "2023-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/generate-template/
feedback: OMRJAVA
title: Generating the form
description: How to render a printable form image and generate a recognition pattern file for Aspose.OMR for Java engine.
keywords:
- render
- page
- form
- print
- paper
- pattern
---

To generate a printable form and a recognition pattern file, provide the path to the form's [source code](/omr/java/design-form/) to `generateTemplate` method of [`OmrEngine`](https://reference.aspose.com/omr/java/com.aspose.omr/omrengine/) class.

```java
OmrEngine engine = new OmrEngine();
GenerationResult res = engine.generateTemplate("source.txt");
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. Optionally, you can [customize](/omr/java/generate-template/page-setup/) the paper size, font, colors, and other layout settings:

```java
OmrEngine engine = new OmrEngine();
GlobalPageSettings pageSettings = new GlobalPageSettings();
pageSettings.FontFamily = "Courier New";
pageSettings.FontSize = 16;
GlobalPageSettings.FontStyle = FontStyle.Italic;
GenerationResult res = engine.generateTemplate("source.txt", pageSettings);
```

## Adding images

Aspose.OMR for Java allows you to personalize machine-readable forms by adding [images](/omr/java/design-form/image/) (such as your company logo or respondent's photo) to them. In addition to describing the element in the source code, the full path to each image file must be directly passed to the form generator.

{{% alert color="caution" %}}
If an image file is mentioned in the source code but no file path is provided, an error will be thrown and the form will not be generated.
{{% /alert %}}

Image paths are provided through the [ImageCollection](https://reference.aspose.com/omr/java/com.aspose.omr/imagecollection/) object. The collection keys must exactly match the names of the image files referenced in the form's source code. For example, if the source code refers to the file _logo.png_ (`?image=logo.png`):

```java
OmrEngine engine = new OmrEngine();
// Configure form layout
GlobalPageSettings pageSettings = new GlobalPageSettings();
pageSettings.PaperSize = PaperSize.Letter;
// Add images
InputStream logoStream = ReadFile("sources/logo.png");
ImageCollection images = new ImageCollection();
images.add("logo.png", logoStream);
// Generate form
GenerationResult res = engine.generateTemplate("source.txt", images, pageSettings);
```

## Saving a printable form

After the template has been successfully generated, you can save it to disk in the preferred format.

The saved results consist of several files:

- Printable form pages as _PNG_ images. Their dimensions match the [provided paper size](/omr/java/generate-template/page-setup/#supported-paper-sizes).
- A recognition pattern used by Aspose.OMR recognition engine, in a special _.OMR_ format. This file is **required** for [recognizing](/omr/java/recognition/) completed forms, make sure you do not accidentally delete it!

To save a form, call `Save` method of of the `GenerationResult` object returned by `generateTemplate` method. The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory of the application.
- File name (without extension) for printable form pages and the recognition pattern.

### Example

```java
OmrEngine engine = new OmrEngine();
GenerationResult res = engine.generateTemplate("source.txt");
res.save("forms", "survey");
```

This code generates the following files under _forms_ sub-directory of the application's working directory:

File | Description
---- | -----------
`survey.png` | An image of a machine-readable form that can be printed and distributed to respondents.
`survey.omr` | Recognition pattern file, that is used to map optical marks to bubbles for highly accurate recognition.

{{% alert color="primary" %}} 
Do not delete or modify recognition pattern (_.OMR_) file. It is required for recognition.

If you have accidentally deleted it, re-generate the form from the source code using exactly the same [page settings](/omr/java/generate-template/page-setup/).
{{% /alert %}}
