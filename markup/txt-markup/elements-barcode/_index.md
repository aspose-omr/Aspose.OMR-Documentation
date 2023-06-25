---
weight: 40
date: "2023-05-30"
author: "Vladimir Lapin"
type: docs
url: /txt-markup/elements-barcode/
feedback: OMRCOMMON
title: Barcodes and QR codes
description: Add barcodes and QR codes to personalize or uniquely identify a form.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
- barcode
- QR code
---

This element adds a barcode or QR code to the form based on the provided string. You can use it to link to your website or to uniquely identify a form (for example, generate personalized exam papers for each student).

Information from the barcode is decoded during recognition.

![QR code](barcode.png)

Aspose.OMT for .NET can generate and recognize a wide variety of barcodes:

- AustralianPosteParcel
- AustraliaPost
- Aztec
- Codabar
- CodablockF
- Code11
- Code128
- Code16K
- Code32
- Code39Extended
- Code39Standard
- Code93Extended
- Code93Standard
- DatabarExpanded
- DatabarExpandedStacked
- DatabarLimited
- DatabarOmniDirectional
- DatabarStacked
- DatabarStackedOmniDirectional
- DatabarTruncated
- DataLogic2of5
- DataMatrix
- DeutschePostIdentcode
- DeutschePostLeitcode
- DotCode
- DutchKIX
- EAN13
- EAN14
- EAN8
- GS1Code128
- GS1DataMatrix
- GS1QR
- IATA2of5
- Interleaved2of5
- ISBN
- ISMN
- ISSN
- ItalianPost25
- ITF14
- ITF6
- MacroPdf417
- Mailmark
- Matrix2of5
- MaxiCode
- MicroPdf417
- MSI
- OneCode
- OPC
- PatchCode
- Pdf417
- Pharmacode
- Planet
- Postnet
- PZN
- QR code
- RM4SCC
- SCC14
- SSCC18
- Standard2of5
- SwissPostParcel
- SwissQR
- UPCA
- UPCE
- VIN

## Syntax

The element is declared with `?barcode=[name]` statement. This statement must be placed on a separate line.

`name` property is used as an element's identifier in recognition results and as a reminder of the element's purpose in template source; for example, "_Web site_". The name is not displayed on the form.

### Attributes

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?barcode=` statement or another attribute, and must begin with a **tab character**.

#### Required

A string encoded as a barcode is provided in **value** attribute. For example: `value=https://products.aspose.com/omr/`.

#### Optional

The **barcode** element can be customized by adding optional attributes to it.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**barcode_type** | QR | Type of the barcode. Can take one of the following values: `AustralianPosteParcel`, `AustraliaPost`, `Aztec`, `Codabar`, `CodablockF`, `Code11`, `Code128`, `Code16K`, `Code32`, `Code39Extended`, `Code39Standard`, `Code93Extended`, `Code93Standard`, `DatabarExpanded`, `DatabarExpandedStacked`, `DatabarLimited`, `DatabarOmniDirectional`, `DatabarStacked`, `DatabarStackedOmniDirectional`, `DatabarTruncated`, `DataLogic2of5`, `DataMatrix`, `DeutschePostIdentcode`, `DeutschePostLeitcode`, `DotCode`, `DutchKIX`, `EAN13`, `EAN14`, `EAN8`, `GS1Code128`, `GS1DataMatrix`, `GS1QR`, `IATA2of5`, `Interleaved2of5`, `ISBN`, `ISMN`, `ISSN`, `ItalianPost25`, `ITF14`, `ITF6`, `MacroPdf417`, `Mailmark`, `Matrix2of5`, `MaxiCode`, `MicroPdf417`, `MSI`, `OneCode`, `OPC`, `PatchCode`, `Pdf417`, `Pharmacode`, `Planet`, `Postnet`, `PZN`, `QR`, `RM4SCC`, `SCC14`, `SSCC18`, `Standard2of5`, `SwissPostParcel`, `SwissQR`, `UPCA`, `UPCE`, `VIN`. | `barcode_type=PDF417`
**qr_version** | Automatic | QR Code version. Only applicable when **barcode_type** is `QR`. | `qr_version=40`
**codetext** | false | Add a string encoded as a barcode below the barcode image. | `codetext=true`
**align** | center | Horizontal alignment of the barcode image: `left`, `center` or `right`. | `align=right`
**height** | Automatic | Barcode height, in pixels. The width is adjusted automatically. | `height=300`
**x** | n/a | Set the absolute position of the barcode relative to the left edge of the page.<br />Overrides the value of **align** attribute. | `x=300`
**y** | n/a | Set the absolute position of the barcode relative to the top edge of the page. | `y=500`

## Allowed child elements

None.

## Example

```
?container=Example
	columns_count=3
?block=Column 1
	column=1
?barcode=Code 39 barcode
	value=Code39
	barcode_type=code39standard
	align=left
	height=150
&block
?block=Column 2
	column=2
?barcode=QR code
	value=https://products.aspose.com/omr/
	height=300
&block
?block=Column 3
	column=3
?barcode=stacked linear barcode
	value=PDF417 Barcode
	barcode_type=PDF417
	codetext=true
	height=300
&block
&container
```

![Barcodes example](barcodes-example.png)
