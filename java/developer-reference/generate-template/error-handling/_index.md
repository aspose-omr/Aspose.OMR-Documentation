---
weight: 20
date: "2023-06-16"
author: "Vladimir Lapin"
type: docs
url: /java/generate-template/error-handling/
feedback: OMRJAVA
title: Error handling
description: Debugging and identifying errors in the Aspose.OMR for Java machine-readable forms.
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

Aspose.OMR for Java offers an easy-to-use method for detecting errors in form's source code. Use `getErrorCode()`, `getErrorMessage()` or `getWarnings()` methods of the [`GenerationResult`](https://reference.aspose.com/omr/java/com.aspose.omr/generationresult/) object returned by the [form generator](/omr/java/generate-template/).

Method | Type | Description
------ | ---- | -----------
`getErrorCode()` | `int` | If the returned value is `0`, the source code is valid and the printable form can be [saved](/omr/java/generate-template/#saving-a-printable-form).
`getErrorMessage()` | `string` | Human-readable error details.
`getWarnings()` | `List<String>` | Human-readable warning messages describing non-critical problems.

Alternatively, you can catch an exception when [saving](/omr/java/generate-template/#saving-a-printable-form) the from.

## Example

```java
OmrEngine engine = new OmrEngine();
GenerationResult res = engine.generateTemplate("source.txt");
if(res.getErrorCode() == 0)
{
	res.Save("target", "omr_form");
}
else
{
	System.out.println(res.getErrorMessage());
}
```
