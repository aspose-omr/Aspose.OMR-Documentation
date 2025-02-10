---
weight: 30
date: "2025-02-10"
author: "Vladimir Lapin"
type: docs
url: /net/generate-template/error-handling/
feedback: OMRNET
title: Error handling
description: Debugging and identifying errors in the source code of the Aspose.OMR template during generation.
keywords:
- render
- page
- form
- print
- error
- exception
- bug
- issue
- fail
---

The source code for complex, deeply nested forms may be very complex and difficult to read. Aspose.OMR offers an easy-to-use method for detecting errors when generating printable forms.

To validate the source code, examine `ErrorCode` property of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`Generate` method](/omr/net/generate-template/). If the property's value is `0`, the source code is valid and the generated form can be [saved](/omr/net/generate-template/save/). Otherwise, there is an error in the source code and you can get a human-readable error in `ErrorMessage` property.

Alternatively, you can catch an exception from `Save` or `SaveAsPdf` methods of of the [`GenerationResult`](https://reference.aspose.com/omr/net/aspose.omr.generation/generationresult) object returned by [`Generate` method](/omr/net/generate-template/).

## Example

```csharp
Aspose.OMR.Api.OmrEngine omrEngine = new Aspose.OMR.Api.OmrEngine();
Aspose.OMR.Generation.GenerationResult generationResult = omrEngine.Generate("source.txt");
if(generationResult.ErrorCode != 0)
{
	Console.WriteLine(generationResult.ErrorMessage);
	return generationResult.ErrorCode;
}
generationResult.Save("", "OMR-Form");
```
