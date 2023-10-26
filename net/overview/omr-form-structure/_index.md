---
weight: 40
date: "2023-10-24"
author: "Vladimir Lapin"
type: docs
url: /net/omr-form-structure/
feedback: OMRNET
title: Aspose.OMR form structure
description: The layout and structure of the Aspose.OMR for .NET printable form and the meaning of its key elements.
keywords:
- page
- marks
- layout
- elements
- design
---

Most OMR-ready forms have a unified structure that allows the recognition engine to reliably associate hand-drawn marks with answers. **Aspose.OMR** uses a special page layout to provide superior recognition accuracy of multi-page forms, photos, and even rotated / skewed images.

![Aspose.OMR form structure](omr-form-structure.png)

## Reference point markers

Located at the corners of the page, these 5 black boxes allow a recognition engine to quickly find inner elements of the form and determine its size and orientation. Reference point markers are crucial for form recognition.

Due to their importance, reference point markers are always rendered above all other elements of the form.

{{% alert color="caution" %}}
**Important considerations:**

- Never remove these markers from the OMR form and do not change their size or position in a graphics editor.
- When scanning or photographing completed forms, ensure that all 5 markers are present in the image.
{{% /alert %}} 

### Rotation marker

This rectangular marker is used to determine page orientation in scans and photographs. It guarantees accurate recognition of skewed, rotated and distorted images.

Position of the rotation marker can be [customized](/omr/net/generate-template/page-setup/#rotation-marker-placement) in page layout settings. 

## Form content

Main area of the form containing response bubbles along with texts, images, and other [elements](/omr/net/design-form/).

## Form footer

An area at the bottom of the page that is primarily used for placing form title, branding information and barcodes.

Footers are manually added to the form's source code using a [**Container** element](/omr/net/design-form/) and may not be present.

## Page identifier

This small QR code only appears on multi-page forms. It contains an encoded identifier of the form and the page number, allowing the recognition engine to treat multiple scanned images as one form.
