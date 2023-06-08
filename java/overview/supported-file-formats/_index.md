---
weight: 30
date: "2023-06-06"
author: "Vladimir Lapin"
type: docs
url: /java/supported-file-formats/
feedback: OMRJAVA
title: Supported file formats
description: File formats for printable templates, scanned or photographed completed forms, and the format of recognition results supported by Aspose.OMR for Java.
keywords:
- format
- image
- data
- source
- template
- result
- scan
- photo
---

## Template sources

Aspose.OMR for Java supports a specialized markup language for designing OMR forms. Form layout is provided in a lightweight text markup language specifically tailored for describing machine-readable forms. It is content-focused, with minimal number of tags or formatting instructions.

The forms can be customized by adding images, such as logos or photos. The images are provided in the following formats:

Format   | Details
-------- | -------
**JPEG** | A widely used format for digital images. Small file size, but image quality may be slightly reduced due to lossy compression.
**PNG**  | An open, extensible image format with lossless compression.


## Printable forms

Once the template source code is ready, you can generate a printable form from it. Aspose.OMR for Java creates 2 files for each form:

File                | Details
------------------- | -------
**{form name}.PNG** | Printable form image in Portable Network Graphics (_.PNG_) format.
**{form name}.OMR** | A recognition pattern used by Aspose.OMR recognition engine, in a special .OMR format (JSON-based).

## Filled forms

Aspose.OMR for Java can recognize scanned or photographed form images:

Extension             | Details
--------------------- | -------
**.JPG**              | JPEG, the most popular format for smartphone photos.
**.PNG**              | Portable Network Graphics.

## Recognition results

Recognition results are returned in the most popular data storage formats that can be imported into any popular database or analysis system:

Format   | Details
-------- | -------
**JSON** | A popular [open standard](https://www.json.org/) format for describing nested data structures. Best suited for NoSQL databases or web.
**CSV**  | A lightweight text format that uses a comma to separate values. Best suited for spreadsheet applications and relational databases.
