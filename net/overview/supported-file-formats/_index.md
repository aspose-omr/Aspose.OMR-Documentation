---
weight: 30
date: "2022-04-12"
author: "Vladimir Lapin"
type: docs
url: /net/supported-file-formats/
title: Supported file formats
description: File and data formats for print forms, scanned / photographed images and recognition results supported by Aspose.OMR for.NET.
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

Aspose.OMR for .NET supports a specialized markup language for designing OMR forms. Form layout can be provided in one of the following formats:

Format     | Details
---------- | -------
**JSON**   | A popular [open standard](https://www.json.org/) file format for describing nested data structures.
**TXT**    | Lightweight text markup specifically tailored for Aspose.OMR forms.
**Object** | Describe the OMR form directly in the application code.

## Print forms

Once the template source code is ready, you can generate a printable document from it. Aspose.OMR for .NET intellectually selects the file format based on the provided extension:

Extension             | Details
--------------------- | -------
**.PDF**              | Portable Document Format, the de facto industry standard for printed documents.
**.JPG**              | JPEG, a widely used format for digital images. Small file size, but image quality may be slightly reduced due to lossy compression.
**.PNG**              | Portable Network Graphics, an open, extensible image format with lossless compression.
**.TIFF** or **.TIF** | Tag Image File Format, abbreviated as _TIFF_ or _TIF_. The most popular high-quality graphics format among artists, photographers and the publishing industry.
**.GIF**              | Small-sized image files that are limited to 256 colors. Best suited for websites and slow networks.
**.BMP**              | Bitmap image file. Supported by almost any device, but the file size can be very large.

## Filled forms

Aspose.OMR for .NET can recognize any file you get from a scanner or camera:

Extension             | Details
--------------------- | -------
**.PDF**              | Portable Document Format (_see the note below_).
**.JPG**              | JPEG, the most popular format for smartphone photos.
**.PNG**              | Portable Network Graphics.
**.TIFF** or **.TIF** | Tag Image File Format, commonly used for high quality scanning (_see the note below_).
**.GIF**              | Graphics Interchange Format. Limited to 256 colors.
**.BMP**              | Bitmap image file.

{{% alert color="primary" %}} 

Recognition of multi-page PDF and TIFF files is not supported. Each page must be scanned as a separate file.

{{% /alert %}} 

## Recognition results

Recognition results are returned in the most popular data storage formats that can be imported into any popular database or analysis system:

Format   | Details
-------- | -------
**JSON** | A popular [open standard](https://www.json.org/) format for describing nested data structures. Best suited for NoSQL databases or web.
**XML**  | Extensible Markup Language, a universal format for most systems.
**CSV**  | A lightweight text format that uses a comma to separate values. Best suited for spreadsheet applications and simple relational database tables.
