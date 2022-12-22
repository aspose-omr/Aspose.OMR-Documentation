---
weight: 20
date: "2022-12-22"
author: "Korobeynikov Nikita"
type: docs
url: /java/images/
title: Adding images
description: How to include images in Aspose.OMR forms.
keywords:
- render
- page
- form
- print
- generate
- image
- picture
---

Aspose.OMR allows you to customize questionnaires, answer sheets, and other forms by adding images (such as your company logo) to them. In addition to describing the element in the form source code, the `java.io.InputStream` to _each_ image file must be directly passed to the [ImageCollection](https://reference.aspose.com/omr/java/com.aspose.omr/ImageCollection).

{{% alert color="primary" %}}

If an image file is mentioned in the source code but no file path is provided, an error will be thrown and the form will not be generated.

{{% /alert %}}

Images can be provided with:

- `com.aspose.omr.ImageCollection` object - a collection of key-value pairs where the key contains the image file name and the value contains the binary content (`java.io.InputStream`) of the image file.

#### Image properties
Field | Description | Default value
--- | ------- | --------
?image=|string value to correspond layout element and `java.io.InputStream`| n/a
height| Height of the inserted image. Set in pixels.  | 200
width | Width of the inserted image. Set in pixels | 200
x | Horizontal coordinate on template layout. Set in pixels. Increments left to right| 210
y | Vertical coordinate on template layout. Set in pixels. Increments top to bottom. </br> | Calculated based on previous elements

#### Image source code example
```
?image=logo.png
	height=300
	width=300
	x=1800
	y=180
```



#### Example of template source code with Image

```
?text=Name__________________________________ Date____________
?grid=ID
	sections_count=8
#What is Aspose.OMR main function?
	() OCR () Capture human-marked data
	() There is no main function () Enhance images
#Can Aspose.OMR process not only scans, but also photos?
	() Yes, indeed! () No
#Aspose.OMR is available on any platform, because it is:
	() Cross-platform code () Cloud service
#Aspose.OMR works with any kind of OMR forms: tests, exams, questionnaires, surveys, etc.
	() Yes, indeed! () No
#Excellent recognition results can be achieved only for filled bubbles at least for:
	() 40% () 60% () 75% () 98%
#Do you have to mark up every question on the page?
	(Yes) Yes, that will help a lot! (No) No
#Rate your preference from 0 to 9 with "0" being preference towards performance
and "9" being preference towards flexibility.
	(0) (1) (2) (3) (4) (5) (6) (7) (8) (9)
#I found aspose omr to be a useful tool. (5 - strongly agree, 1 - strongly disagree)
	(5) (4) (3) (2) (1)

?text= Answer sheet section
?answer_sheet=MainQuestions
	elements_count=10
	columns_count=5

?text=Sign________________________________

?image=logo.png
	height=300
	width=300
	x=1800
	y=180
```

## Generate and save the printable form, providing image with FileInputStream:

```java
OmrEngine engine = new OmrEngine();

ImageCollection collection = new ImageCollection();
String logoPath = "path\to\the\logo.png";
FileInputStream logoStream = new FileInputStream(logoPath);
collection.add("logo.png", logoStream);

GenerationResult res = engine.generateTemplate(markupPath, collection);
res.Save("path\to\the\output_directory","template_name");

```


{{% alert color="primary" %}}

If the same image file is mentioned in the form source code multiple times it is **required** to pass **resetable** InputStream. e.g. ByteArrayInputStream

{{% /alert %}}


## Generate and save the printable form, providing image with resetable InputStream:

#### Resetable stream
```java
private ByteArrayInputStream ReadFile(String filepath){
		File file = new File(filepath);

		FileInputStream fileStream = new FileInputStream(file);

		// Now creating byte array of same length as file
		byte[] arr = new byte[(int)file.length()];

		// Reading file content to byte array
		// using standard read() method
		fileStream.read(arr);

		// lastly closing an instance of file input stream
		// to avoid memory leakage
		fileStream.close();

		return new ByteArrayInputStream(arr);
    }
```

Generate and save the printable form, loading images from memory:

```java
OmrEngine engine = new OmrEngine();

ImageCollection collection = new ImageCollection();
String logoPath = "path\to\the\logo.png";
//ReadFile implementation see above
collection.add("logo.png", ReadFile(logoPath));

GenerationResult res = engine.generateTemplate(markupPath, collection);
res.Save("path\to\the\output_directory","template_name");
```

#### Generated image
![Template with image](template.png)



