---
weight: 40
date: "2022-05-30"
author: "Vladimir Lapin"
type: docs
url: /net/programmatic-forms/elements-barcode/
title: Barcodes and QR codes
description: Add barcodes and QR codes to personalize or uniquely identify a form.
keywords:
- layout
- markup
- template
- design
- form
- code
- object
- C#
- barcode
- QR code
---

This element adds a barcode or QR code to the form based on the provided string. You can use it to link to your website or to uniquely identify a form (for example, generate personalized exam papers for each student).

Information from the barcode is decoded during recognition.

![QR code](program-barcode.png)

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

## Declaration

This element is declared as an instance of [`BarcodeConfig`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config.elements/barcodeconfig/) class. Reference `Aspose.OMR.Generation.Config.Elements` and `Aspose.OMR.Generation.Config.Enums` namespaces to use `ContentConfig` types without specifying the fully qualified namespace:

```csharp
using Aspose.OMR.Generation.Config.Elements;
using Aspose.OMR.Generation.Config.Enums;
```

A string encoded as a barcode is specified in the **Value** property.

```csharp
new BarcodeConfig() {
	Value = "Encoded string"
}
```

### Required properties

Name | Type | Description
---- | ---- | -----------
**Value** | string | A string encoded as a barcode.

### Optional properties

Name | Type | Default value | Description
---- | ---- | ------------- | -----------
**Name** | `string` | _n/a_ | Used as an element's identifier in recognition results and as a reminder of the element's purpose in template source; for example, "_Web site_".<br />This text is not displayed on the form.
**BarcodeType** | [Barcode type](https://apireference.aspose.com/barcode/net/aspose.barcode.generation/encodetypes/) | _QR Code_ | Type of the barcode.
**BarcodeQRVersion** | [`Aspose.BarCode.Generation.QRVersion`](https://apireference.aspose.com/barcode/net/aspose.barcode.generation/qrversion/) | _Automatic_ | QR Code version. Only applicable when `BarcodeType` is `QR`.
**DrawCodetext** | `bool` | false | Add a string from the `Value` property below the barcode image.
**Align** | [`AlignmentEnum`](https://apireference.aspose.com/omr/net/aspose.omr.generation.config.enums/alignmentenum/) | `AlignmentEnum.Center` | Horizontal alignment of the barcode image.
**Height** | `int` | _Automatic_ | Barcode height, in pixels. The width is adjusted automatically.
**X** | `int` | _n/a_ | Set the absolute position of the barcode relative to the left edge of the page.<br />Overrides the value of `Align` property.
**Y** | `int` | _n/a_ | Set the absolute position of the barcode relative to the top edge of the page.

## Allowed child elements

None.

## Example

```csharp
TemplateConfig templateConfig = new TemplateConfig() {
	Children=new List<BaseConfig>() {
		new PageConfig() {
			Children = new List<BaseConfig>() {
				new ContainerConfig() {
					Name = "Example",
					ColumnsCount = 2,
					Children= new List<BaseConfig>() {
						new BlockConfig() {
							Column = 1,
							Children = new List<BaseConfig>() {
								new BarcodeConfig() {
									Value = Guid.NewGuid().ToString(),
									Align = AlignmentEnum.Left,
									Height = 300
								}
							}
						},
						new BlockConfig() {
							Column = 2,
							Children = new List<BaseConfig>() {
								new BarcodeConfig() {
									Value = "John Doe",
									Align = AlignmentEnum.Left,
									DrawCodetext = true,
									Height = 300
								}
							}
						}
					}
				}
			}
		}
	}
};
```

![Barcodes example](barcodes-example.png)
