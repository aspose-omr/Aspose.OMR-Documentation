---
weight: 10
date: "2022-04-20"
author: "Vladimir Lapin"
type: docs
url: /net/txt-markup/
aliases:
- /net/template-generation/txt/
- /net/template-generation/txt/elements-description/
title: Text markup
description: Lightweight markup language specifically tailored for creating Aspose.OMR forms.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
---

Aspose.OMR **text markup** is a lightweight markup language specifically tailored for describing content and layout of Aspose.OMR forms. It is content-focused, with minimal number of tags or formatting instructions.

The downsides of text markup are that it doesn't support syntax highlighting and is somewhat harder to read when working with nested layouts.

Template sources are stored as plain-text files that can be opened with any general-purpose text editor or code editor (such as **Notepad** or **Visual Studio Code**). The following encodings are supported:

- **UTF-8**, with or without BOM (byte order mark). Recommended encoding that can accommodate forms in any combination of natural languages, including Chinese, Arabic, Hindi, Hebrew, and more.
- **ANSI** - for forms that use Western European characters only.

You can use Windows (_CRLF_), Unix (_LF_) and Mac OS 9 (_CR_) line endings.

## Elements

**Text** markup includes a wide range of elements that allow you to create OMR forms of any complexity - from a simple ballot to high school exam papers and finance application checklists.

- [Layout](/omr/net/txt-markup/elements-layout/)  
  Arrange other elements; define the appearance and design of OMR forms.
- [Questionnaires](/omr/net/txt-markup/elements-questionnaire/)  
  Build OMR-ready surveys, ballots, checklists, and similar forms.
- [Answer sheets](/omr/net/txt-markup/elements-bubble-matrix/)  
  Populate a form with a grid of bubbles representing answers to an exam, test, or assessment.
- [Barcodes and QR codes](/omr/net/txt-markup/elements-barcode/)  
  Add barcodes and QR-codes to personalize or uniquely identify a form.
- [Write-ins](/omr/net/txt-markup/write_in/)  
  Provide a blank field in which the respondent can hand write some text or draw a picture.

## Examples

Check out [code examples](/omr/net/txt-markup/examples/) to see how different elements can be used and combined with each other.
