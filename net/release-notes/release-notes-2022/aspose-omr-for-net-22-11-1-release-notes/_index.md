---
weight: 20
date: "2022-11-25"
author: "Vladimir Lapin"
type: docs
url: /net/aspose-omr-for-net-22-11-1-release-notes/
title: Aspose.OMR for .NET 22.11.1 Release Notes
description: A summary of recent changes, enhancements and bug fixes in Aspose.OCR for .NET 22.11.1 (November 2022) release.
keywords:
- 2022
- November
- new
- release
- changelog
---

{{% alert color="primary" %}} 
This article contains a summary of recent changes, enhancements and bug fixes in [**Aspose.OMR for .NET 22.11.1 (November 2022)**](https://www.nuget.org/packages/Aspose.OMR/22.11.1) release.
{{% /alert %}} 

## What was changed

Key | Summary | Category
--- | ------- | --------
OMRNET-351 | Added support for .NET 6 | Enhancement

## Known issues and limitations

Key | Summary | Workaround
--- | ------- | ----------
OMRNET-462 | Recognition of multi-page PDF and TIFF files causes an error. | Scan each page of the filled form into a separate file and recognize them one-by-one.
OMRNET-555 | [`Recalculate`](https://reference.aspose.com/omr/net/aspose.omr.api/templateprocessor/recalculate/) method results in incorrect processing of **ScoreGroup** elements ([text markup](/omr/net/txt-markup/score_group/) / [JSON markup](/omr/net/json-markup/scoregroup/)) and **CustomAnswerSheet** elements ([text markup](/omr/net/txt-markup/custom_answer_sheet/) / [JSON markup](/omr/net/json-markup/customanswersheet/)). | Use [`RecognizeImage`](https://reference.aspose.com/omr/net/aspose.omr.api/templateprocessor/recognizeimage/) method with different threshold setting instead of [run-time adjustments of recognition accuracy](/omr/net/recognition/accuracy-threshold/#adjusting-recognition-accuracy-at-run-time).
OMRNET-685 | Texts in **ChoiceBox** elements ([text markup](/omr/net/txt-markup/question/) / [JSON markup](/omr/net/json-markup/choicebox/)) are not automatically wrapped to fit the parent. | Set line breaks manually to match the width of the parent element / page.

## Public API changes and backwards compatibility

This section lists all public API changes introduced in **Aspose.OMR for .NET 22.11.1** that may affect the code of existing applications.

### Added public APIs:

_No changes._

### Updated public APIs:

_No changes._

### Removed public APIs:

_No changes._
