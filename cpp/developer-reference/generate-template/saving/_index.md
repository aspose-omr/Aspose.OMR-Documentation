---
weight: 20
date: "2023-06-23"
author: "Vladimir Lapin"
type: docs
url: /cpp/generate-template/save/
feedback: OMRCPP
title: Saving a printable form and recognition pattern
description: How to save a generated printable form image and a recognition pattern file on disk.
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

After the template has been successfully [generated](/omr/cpp/generate-template/), you can save it to disk in the preferred format. The saved results consist of several files:

- Printable form pages as PNG images. Their dimensions match the [provided](/omr/cpp/generate-template/page-setup/) paper size and orientation.  
  Each page is always saved as a separate file. If multiple pages are generated, the suffix "_Page{NUMBER}_" will be added to each file; for example, "_OMR-FormPage1.png_".
- A recognition pattern used by Aspose.OMR for C++ recognition engine, in a special _.OMR_ format. This file is **required** for [recognizing](/omr/cpp/recognition/) filled forms, make sure you do not accidentally delete it!

To save a form, call `Save` method of of the `GenerationResult` object returned by `GenerateTemplate` method. The method takes the following arguments:

- Target directory name, either absolute or relative to your application's working directory. Provide an empty string to save files into the working directory of the application.
- File name (without extension) for printable form pages and the recognition pattern.

Printable pages are saved as _PNG_ images.

### Example

```csharp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Generation::GenerationResult> result = engine->GenerateTemplate(u"source.txt");
result.Save("", "OMR-Form");
```

This code generates the following files under _forms_ sub-directory of the application's working directory:

File | Description
---- | -----------
`OMR-Form.png` | An image of a machine-readable form that can be printed and distributed to respondents.
`OMR-Form.omr` | Recognition pattern file, that is used to map optical marks to bubbles for highly accurate recognition.

{{% alert color="primary" %}} 
Do not delete or modify recognition pattern (_.OMR_) file. It is required for recognition.

If you have accidentally deleted it, re-generate the form from the source code using exactly the same [page settings](/omr/cpp/generate-template/page-setup/).
{{% /alert %}}
