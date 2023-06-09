---
weight: 30
date: "2023-06-08"
author: "Vladimir Lapin"
type: docs
url: /cpp/supported-file-formats/
feedback: OMRCPP
title: Supported file formats
description: File formats supported by Aspose.OMR for C++ for printing templates, scaning or taking a photo of completed forms, and returning recognition results.
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

Aspose.OMR for C++ supports a specialized markup language for designing OMR forms. Form layout is provided in a lightweight text markup language specifically tailored for describing machine-readable forms. It is content-focused, with minimal number of tags or formatting instructions.

The forms can be customized by adding images, such as logos or photos. The images are provided in the following formats:

Format   | Details
-------- | -------
**JPEG** | A widely used format for digital images. Small file size, but image quality may be slightly reduced due to lossy compression.
**PNG**  | An open, extensible image format with lossless compression.
**BMP**  | Bitmap image file. Supported by almost any device, but the file size can be very large.

## Printable forms

Once the template source code is ready, you can generate a printable form from it. Aspose.OMR for C++ creates 2 files for each form:

File                | Details
------------------- | -------
**{form name}.PNG** | Printable form image in Portable Network Graphics (_.PNG_) format.
**{form name}.OMR** | A recognition pattern used by Aspose.OMR recognition engine, in a special _.OMR_ format (JSON-based).

## Filled forms

Aspose.OMR for C++ can recognize scanned or photographed form images:

Format   | Details
-------- | -------
**JPEG** | A widely used format for digital images. Small file size, but image quality may be slightly reduced due to lossy compression.
**PNG**  | An open, extensible image format with lossless compression.
**BMP**  | Bitmap image file. Supported by almost any device, but the file size can be very large.

## Recognition results

Recognition results are returned in the most popular data storage formats that can be imported into any popular database or analysis system:

Format   | Details
-------- | -------
**JSON** | A popular [open standard](https://www.json.org/) format for describing nested data structures. Best suited for NoSQL databases or web.
**CSV**  | A lightweight text format that uses a comma to separate values. Best suited for spreadsheet applications and relational databases.
