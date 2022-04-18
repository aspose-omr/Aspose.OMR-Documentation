---
title: English test (.txt)
type: docs
weight: 5
url: /net/showcases/english/txt
---

{{% alert color="primary" %}} 

This example constructed for custom GlobalPageSettings. Please use provided settings from text below for best result.

{{% /alert %}}


**Template generation call**

<details>
<summary>C# Code</summary>

````java
var license = new License();
license.SetLicense(@"C:\Users\User\Desktop\Aspose.license");

var engine = new OmrEngine();
var settings = new GlobalPageSettings
{
	PaperSize = PaperSize.Letter,
	Orientation = Orientation.Vertical,
	BubbleColor = Color.Black,
	BubbleSize = BubbleSize.Small,
	FontStyle = FontStyle.Regular,
	FontSize = 9,
	FontFamily = "Segoe UI",
	ImagesPaths = images
};
var configPath = @"C:\Users\User\Desktop\template\template.txt";

var result = engine.GenerateTemplate(configPath, settings);
result.Save(@"C:\Users\User\Desktop\template", "generated_template");
````

</details>

**Template TXT markdown**

<details>
<summary>TXT markdown</summary>

```text
?empty_line=start
	height=5
?container=1
	columns_count=1
?block=2
	column=1
	border=none
?image=icon.jpg
	x=200
	y=100
	height=200
	width=200
?content=WEST BOARD OF SECONDARY EDUCATION
	font_size=10
	font_family=Segoe UI
	font_style=bold
	align=Right	
&block
&container
?container=co2
	columns_count=2
?block=b2
	column=1
?content=ANSWER SHEET
	align=Right
	font_style=bold
	font_size=10
?content=USE ONLY BLUE/BLACK BALLPOINT PEN
	font_size=6
	align=Right
&block
?block=b3
	column=2
?content=Secondary School Examination (Class X)
	align=center
	font_style=bold
	font_size=10
&block
&container
?container=c344
	columns_count=2
?block=b34
	border=square
	column=1
?input_group=b344
	input_border=square
?content=Roll No.
	font_size=6
?content=   12681458
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=(in digits and words)
	font_size=6
?content=twelve million six hundred and eighty-one thousand four hundred and fifty-eight
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=Center No. & name
	font_size=6
?content=1001 West High School
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=Subject code & name
	font_size=6
?content=301 - ENGLISH CORE
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=Teacher name
	font_size=6
?content=Sam Jonathan Williams
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=First name
	font_size=6
?content=John
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=Middle name
	font_size=6
?content=Williams
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=Last name
	font_size=6
?content=Smith
	align=left
	font_size=6
&input_group
?input_group=b344
	input_border=square
?content=School code and name
	font_size=6
?content=(10005) West High School
	align=left
	font_size=6
&input_group
?input_group=b433
	input_border=square
?content=State
	font_size=6
?content=Texas
	align=left
	font_size=6
&input_group
&block
?block=
	border=square
	column=2
?paragraph=barcode omr
?empty_line=
	height=25
?content=OMR No. 1387342325
	font_size=9
	align=center
?barcode=1
	value=1387342325
	height=100
	X=1270
	Y=390
	codetext=false
	barcode_type=Code128
&paragraph
&block
?block=12312
	border=square
	is_clipped=true
	column=2
?content=Examination date
	align=center
	font_size=10
	align=center
?empty_line=
	height=55
?content=  /  /    
	content_type=Cells
	align=center
&block
?block=12312
	border=square
	is_clipped=true
	column=2
?content=Question Paper Code
	font_size=10
	align=center
?empty_line=
	height=55
?content=    /  /  
	content_type=Cells
	align=center
&block
&container
?container=
	columns_count=1
?block=
	column=1
	border=square
?content=Select answer option by filling circle.
	font_size=8
	font_style=bold
?content=For your own answer fill in empty square under "*" column.
	font_size=8
	font_style=bold 
?content=To withdraw your answer fill circle under "#" column.
	font_size=8
	font_style=bold
&block
&container
?container=custom_answer_sheet_container
	columns_count=1
?block=all
	column=1
	border=square
?custom_answer_sheet=72 questions
	section_border=square
	amount=72
	columns_count=3
	row_proportions=15%-55%-15%-15%
?header=123
?column=QNo.
	font_size=4
	font_style=bold
	align=center
?column=Bubbles
	font_size=4
	font_style=bold
	align=center
?column=*
	font_size=4
	font_style=bold
	align=center
?column=#
	font_size=4
	font_style=bold
	align=center
&header
?custom_row=row_%index%
?content=%index%
	font_size=9
	font_style=regular
	align=center
?bubble_array=b_%index%
	font_size=6
	font_style=regular
	answers_list=(A)(B)(C)(D)
	bubble_size=extrasmall
?write_in=customWriteIn
	required=true
?custom_trigger=trigger_to_skip_question
	trigger_type=replaceValue
	value=question skipped
	target=60 questions_%index%
	bubble_size=extrasmall
&custom_row
&custom_answer_sheet
?empty_line=
	height=20
&block
&container
?container=123
	columns_count=1
?block=
	column=1
	border=square
	is_clipped=true
?empty_line=
	height=60
?content=Candidate's Signature
	align=right
	font_size=8
&block
&container
?container=total_answers
	columns_count=4
?block=all
	is_clipped=true
	border=square
?block=left1
	column=1
	border=none
?content=Total correct answers
	align=left
	font_style=bold
	font_size=8
?content=(To be filled by the Evaluator)
	align=left
	font_style=bold
	font_size=6
&block
?block=left2
	column=2
	border=none
?content=  
	content_type=Cells
	align=center
&block
?block=right1
	column=3
	border=none
?content=Total correct answers
	align=left
	font_style=bold
	font_size=8
?content=(To be filled by the Coordinator)
	align=left
	font_style=bold
	font_size=6
&block
?block=right2
	column=4
	border=none
?content=  
	content_type=Cells
	align=center
&block
?empty_line=
	height=1
&block
&container
?container=signatures
	columns_count=1
?block=
	column=1
	is_clipped=true
?table=signature_table
	answers_count=4
	table_type=equalcells
?table_header=header
	font_style=bold
?content=
?content=Invigilator
	font_style=bold
	font_size=8
	align=center
?content=Evaluator
	font_style=bold
	font_size=8
	align=center
?content=Coordinator
	font_style=bold
	font_size=8
	align=center
?content=Observer
	font_style=bold
	font_size=8
	align=center
&table_header
?content=Signature
	font_style=bold
	font_size=8
	align=center
?content=Identification No.
	font_style=bold
	font_size=8
	align=center
&table
&block
&container
```

</details>

**Template result**

**![todo:image_alt_text](english-txt.png)**