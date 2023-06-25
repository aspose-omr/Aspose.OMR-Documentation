---
weight: 30
date: "2023-06-23"
author: "Vladimir Lapin"
type: docs
url: /cpp/generate-template/
feedback: OMRCPP
title: Generating the template
description: How to render a printable form image and generate a recognition pattern file for Aspose.OMR for C++ engine.
keywords:
- render
- page
- form
- print
- paper
- pattern
---

To generate a form image that can be printed out and handled to respondents, process the form's [source code](/omr/cpp/design-form/) with `GenerateTemplate` method.

```cpp
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Generation::GenerationResult> result = engine->GenerateTemplate(u"source.txt");
```

It will create a printable form for _A4 (210 x 297 mm)_ paper in _portrait (vertical)_ orientation using the default font and colors. You can [customize](/omr/cpp/generate-template/page-setup/) the paper size, orientation, font, colors and other layout settings that apply to all template pages, as well as specify paths to images used in the form by passing `GlobalPageSettings` object to the method.

If your form contains images, pass the absolute path to each image file in a string array:

```cpp
const char* images[1] = {
	u"aspose-logo.png"
};
System::SharedPtr<Api::OmrEngine> engine = System::MakeObject<Api::OmrEngine>();
System::SharedPtr<Generation::GenerationResult> result = engine->GenerateTemplate(u"source.txt", images);
```

## Read more

- [Page setup](/omr/cpp/generate-template/page-setup/) - customizing the paper size, orientation, font, images, and other layout settings of a printable form.
- [Saving to file](/omr/cpp/generate-template/save/) - saving a generated printable form and a recognition pattern file on disk.
