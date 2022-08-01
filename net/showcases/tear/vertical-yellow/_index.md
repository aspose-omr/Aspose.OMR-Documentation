---
weight: 60
date: "2022-06-03"
author: "Vladimir Lapin"
type: docs
url: /net/showcases/tear/vertical-yellow/
title: Yellow OMR form with a vertical tear line
description: OMR form with a vertical tear line in yellow
keywords:
- examples
- branding
- survey
- source
- double
- tear line
---

Two identical forms on one sheet separated with a horizontal or vertical tear line. Both parts are filled identically; one part remains with the respondent.

![Yellow OMR form with a vertical tear line template](vertical-tear-line.png)

## Source code

<details>
<summary>Text markup</summary>

```
?container=main
	columns_proportions=46%-8%-46%
	block_bottom_margin=0
	block_top_padding=0
	block_right_margin=0
?block=left-header
	column=1
?paragraph=
?image=logo.jpg
	height=200
	width=200
	align=center
?content=Aspose Board
	font_style=bold
	font_size=18
	align=center
?content=of education
	font_style=bold
	font_size=18
	align=center
?content=Personalized Test
	font_style=bold
	font_size=12
	align=center
&paragraph
&block
?block=left-header
	column=1
	border=square
	border_color=DarkOrange
?content=Personal Info
	font_size=12
	align=center
	font_style=bold, italic
&block
?block=left-header-description
	column=1
	border=square
	border_color=DarkOrange
?content=Please check your name and school. Make sure it is your personal information. Make sure spelling is correct.
	font_size=6
	align=right
	font_style=italic
&block
?block=left-content
	column=1
	border=square
	border_color=DarkOrange
?input_group=first_name
	input_border=none
?content=First name
?content=John
	align=center
&input_group
?input_group=middle_name
	input_border=none
?content=Middle name
?content=Gavin
	align=center
&input_group
?input_group=last_name
	input_border=none
?content=Last name
?content=Malkovich 
	align=center
&input_group
?input_group=school
	input_border=none
?content=School
?content=Aspose High School
	align=center
&input_group
&block
?block=left_space
	column=1
	border=none
?empty_line=
	height=100
&block
?block=left_section_1_header
	column=1
	border=square
	border_color=DarkOrange
?content=Section 1
	font_size=12
	align=center
	font_style=bold, italic
?empty_line=50
	height=50
&block
?block=left_section_1_content
	column=1
	border=square
	border_color=DarkOrange
?empty_line=25
	height=25
?answer_sheet=SEC1.
	column=1
	elements_count=6
	columns_count=1
	answers_count=11
?empty_line=25
	height=25
&block
?block=left_space
	column=1
	border=none
?empty_line=
	height=100
&block
?block=left_section_2_header
	column=1
	border=square
	border_color=DarkOrange
?content=Section 2
	font_size=12
	align=center
	font_style=bold, italic
?empty_line=50
	height=50
&block
?block=left_section_2_content
	column=1
	border=square
	border_color=DarkOrange
?empty_line=25
	height=25
?answer_sheet=SEC2..
	column=1
	elements_count=6
	columns_count=1
	answers_count=11
?empty_line=25
	height=25
&block
?block=left_footer
	column=1
?empty_line=50
	height=150
?barcode=test_id
	codetext=true
	value=15478977
	barcode_type=Code32
&block
?block=right-header
	column=3
?paragraph=
?image=logo.jpg
	height=200
	width=200
?content=Aspose Board
	font_style=bold
	font_size=18
	align=center
?content=of education
	font_style=bold
	font_size=18
	align=center	
?content=Personalized Test
	font_style=bold
	font_size=12
	align=center
&paragraph
&block
?block=right-header
	column=3
	border=square
	border_color=DarkOrange
?content=Personal Info
	font_size=12
	align=center
	font_style=bold, italic
&block
?block=right-header-description
	column=3
	border=square
	border_color=DarkOrange
?content=Please check your name and school. Make sure it is your personal information. Make sure spelling is correct.
	font_size=6
	align=right
	font_style=italic
&block
?block=right-personal-content
	column=3
	border=square
	border_color=DarkOrange
?input_group=first_name
	input_border=none
?content=First name
?content=Andrew
	align=center
&input_group
?input_group=middle_name
	input_border=none
?content=Middle name
?content=Willson
	align=center
&input_group
?input_group=last_name
	input_border=none
?content=Last name
?content=Smith 
	align=center
&input_group
?input_group=school
	input_border=none
?content=School
?content=Aspose High School
	align=center
&input_group
&block
?block=right_space
	column=3
	border=none
?empty_line=
	height=100
&block
?block=right_section_1_header
	column=3
	border=square
	border_color=DarkOrange
?content=Section 1
	font_size=12
	align=center
	font_style=bold, italic
?empty_line=50
	height=50
&block
?block=right_section_1_content
	column=3
	border=square
	border_color=DarkOrange
?empty_line=25
	height=25
?answer_sheet=SEC1.
	column=3
	start_id=1
	elements_count=6
	columns_count=1
	answers_count=11
?empty_line=25
	height=25
&block
?block=right_space
	column=3
	border=none
?empty_line=
	height=100
&block
?block=right_section_2_header
	column=3
	border=square
	border_color=DarkOrange
?content=Section 2
	font_size=12
	align=center
	font_style=bold, italic
?empty_line=50
	height=50
&block
?block=right_section_2_content
	column=3
	border=square
	border_color=DarkOrange
?empty_line=25
	height=25
?answer_sheet=SEC2..
	column=3
	start_id=7
	elements_count=6
	columns_count=1
	answers_count=11
?empty_line=25
	height=25
&block
?block=right_footer
	column=3
?empty_line=50
	height=150
?barcode=test_id
	codetext=true
	value=15478977
	barcode_type=Code32
&block
&container
?image=tear-line.png
	x=1200
	y=0
	width=150
	height=3295
```

</details>

<details>
<summary>JSON markup</summary>

```json
{
  "name": null,
  "children": [
    {
      "name": null,
      "children": [
        {
          "name": "main",
          "children": [
            {
              "name": "left-header",
              "children": [
                {
                  "name": "",
                  "children": [
                    {
                      "align": "Center",
                      "name": "logo.jpg",
                      "image_path": null,
                      "x": -1,
                      "y": -1,
                      "height": 200,
                      "width": 200,
                      "element_type": "Image"
                    },
                    {
                      "name": "Aspose Board",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 18,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    },
                    {
                      "name": "of education",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 18,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    },
                    {
                      "name": "Personalized Test",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 12,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "paragraph_type": "Normal",
                  "element_type": "Paragraph"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left-header",
              "children": [
                {
                  "name": "Personal Info",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left-header-description",
              "children": [
                {
                  "name": "Please check your name and school. Make sure it is your personal information. Make sure spelling is correct.",
                  "font_family": "Calibri",
                  "font_style": "Italic",
                  "font_size": 6,
                  "content_type": "Normal",
                  "align": "Right",
                  "element_type": "Content"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left-content",
              "children": [
                {
                  "name": "first_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "First name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "John",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "middle_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "Middle name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Gavin",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "last_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "Last name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Malkovich ",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "school",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "School",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Aspose High School",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_space",
              "children": [
                {
                  "name": "",
                  "height": 100,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_section_1_header",
              "children": [
                {
                  "name": "Section 1",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "50",
                  "height": 50,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_section_1_content",
              "children": [
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                },
                {
                  "bubble_size": "Normal",
                  "name": "SEC1.",
                  "column": 1,
                  "elements_count": 6,
                  "columns_count": 1,
                  "answers_count": 11,
                  "start_id": -1,
                  "vertical_margin": 0,
                  "bubble_type": "Round",
                  "answers_list": null,
                  "element_type": "AnswerSheet"
                },
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_space",
              "children": [
                {
                  "name": "",
                  "height": 100,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_section_2_header",
              "children": [
                {
                  "name": "Section 2",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "50",
                  "height": 50,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_section_2_content",
              "children": [
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                },
                {
                  "bubble_size": "Normal",
                  "name": "SEC2..",
                  "column": 1,
                  "elements_count": 6,
                  "columns_count": 1,
                  "answers_count": 11,
                  "start_id": -1,
                  "vertical_margin": 0,
                  "bubble_type": "Round",
                  "answers_list": null,
                  "element_type": "AnswerSheet"
                },
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "left_footer",
              "children": [
                {
                  "name": "50",
                  "height": 150,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "test_id",
                  "value": "15478977",
                  "barcode_type": "Code32",
                  "qr_version": "Auto",
                  "align": "Center",
                  "height": -1,
                  "codetext": true,
                  "X": -1,
                  "Y": -1,
                  "element_type": "Barcode"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right-header",
              "children": [
                {
                  "name": "",
                  "children": [
                    {
                      "align": "Center",
                      "name": "logo.jpg",
                      "image_path": null,
                      "x": -1,
                      "y": -1,
                      "height": 200,
                      "width": 200,
                      "element_type": "Image"
                    },
                    {
                      "name": "Aspose Board",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 18,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    },
                    {
                      "name": "of education",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 18,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    },
                    {
                      "name": "Personalized Test",
                      "font_family": "Calibri",
                      "font_style": "Bold",
                      "font_size": 12,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "paragraph_type": "Normal",
                  "element_type": "Paragraph"
                }
              ],
              "column": 3,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right-header",
              "children": [
                {
                  "name": "Personal Info",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right-header-description",
              "children": [
                {
                  "name": "Please check your name and school. Make sure it is your personal information. Make sure spelling is correct.",
                  "font_family": "Calibri",
                  "font_style": "Italic",
                  "font_size": 6,
                  "content_type": "Normal",
                  "align": "Right",
                  "element_type": "Content"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right-personal-content",
              "children": [
                {
                  "name": "first_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "First name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Andrew",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "middle_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "Middle name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Willson",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "last_name",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "Last name",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Smith ",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                },
                {
                  "name": "school",
                  "element_type": "InputGroup",
                  "children": [
                    {
                      "name": "School",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "Aspose High School",
                      "font_family": "Calibri",
                      "font_style": "Regular",
                      "font_size": 10,
                      "content_type": "Normal",
                      "align": "Center",
                      "element_type": "Content"
                    }
                  ],
                  "label_border": "None",
                  "input_border": "None",
                  "border_size": 3,
                  "border_color": "Black"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_space",
              "children": [
                {
                  "name": "",
                  "height": 100,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_section_1_header",
              "children": [
                {
                  "name": "Section 1",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "50",
                  "height": 50,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_section_1_content",
              "children": [
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                },
                {
                  "bubble_size": "Normal",
                  "name": "SEC1.",
                  "column": 3,
                  "elements_count": 6,
                  "columns_count": 1,
                  "answers_count": 11,
                  "start_id": 1,
                  "vertical_margin": 0,
                  "bubble_type": "Round",
                  "answers_list": null,
                  "element_type": "AnswerSheet"
                },
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_space",
              "children": [
                {
                  "name": "",
                  "height": 100,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_section_2_header",
              "children": [
                {
                  "name": "Section 2",
                  "font_family": "Calibri",
                  "font_style": [
                    "Bold",
                    "Italic"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "50",
                  "height": 50,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_section_2_content",
              "children": [
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                },
                {
                  "bubble_size": "Normal",
                  "name": "SEC2..",
                  "column": 3,
                  "elements_count": 6,
                  "columns_count": 1,
                  "answers_count": 11,
                  "start_id": 7,
                  "vertical_margin": 0,
                  "bubble_type": "Round",
                  "answers_list": null,
                  "element_type": "AnswerSheet"
                },
                {
                  "name": "25",
                  "height": 25,
                  "element_type": "EmptyLine"
                }
              ],
              "column": 3,
              "border": "Square",
              "border_size": 3,
              "border_color": "DarkOrange",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "right_footer",
              "children": [
                {
                  "name": "50",
                  "height": 150,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "test_id",
                  "value": "15478977",
                  "barcode_type": "Code32",
                  "qr_version": "Auto",
                  "align": "Center",
                  "height": -1,
                  "codetext": true,
                  "X": -1,
                  "Y": -1,
                  "element_type": "Barcode"
                }
              ],
              "column": 3,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 0,
          "columns_proportions": [
            46,
            8,
            46
          ],
          "container_type": "Normal",
          "block_right_margin": 0,
          "block_bottom_margin": 0,
          "block_top_padding": 0,
          "element_type": "Container"
        },
        {
          "align": "Center",
          "name": "tear-line.png",
          "image_path": null,
          "x": 1200,
          "y": 0,
          "height": 3295,
          "width": 150,
          "element_type": "Image"
        }
      ],
      "element_type": "Page"
    }
  ],
  "element_type": "Template"
}
```

</details>

## Page settings

This template was generated using the following paper size, orientation, font, and other [layout settings](/omr/net/generate-template/page-setup/):

```csharp
GlobalPageSettings settings = new GlobalPageSettings
{
    PaperSize = PaperSize.Letter,
    Orientation = Orientation.Vertical,
    BubbleColor = Color.DarkOrange,
    BubbleSize = BubbleSize.Normal,
    FontStyle = FontStyle.Regular,
    FontSize = 10,
    FontFamily = "Calibri",
};
```

## Recognition results

![Yellow OMR form with a vertical tear line filled](vertical-tear-line-recognized.png)

```
Element Name,Value,
SEC11,"A"
SEC11,"D"
SEC12,"K"
SEC12,"C"
SEC13,"B,J"
SEC13,"C,J"
SEC14,"E"
SEC14,"H"
SEC15,"H"
SEC15,"E"
SEC16,"G"
SEC16,"G"
SEC27,""
SEC27,"K"
SEC28,"A"
SEC28,"J"
SEC29,"A,H"
SEC29,"B,K"
SEC210,"C,H,J"
SEC210,"B,G"
SEC211,"C,F"
SEC211,"D,G"
SEC212,"D"
SEC212,"E"
test_id,"154789770"
test_id,"154789770"
```

## Download

[Click here](https://github.com/aspose-omr/Aspose.OMR-Documentation/blob/master/net/showcases/download/tearline-vertical-yellow.zip) to download full template sources and related files. 

**Package structure:**

File | Description
---- | -----------
**logo.jpg** | company logo
**settings.json** | [page settings](/omr/net/generate-template/page-setup/)
**tear-line.png** | vertical tear line image
**vertical tear-line.csv** | recognition results based on the filled form available in this package
**vertical tear-line.json** | source code in [JSON markup](/omr/net/json-markup/)
**vertical tear-line.omr** | recognition pattern
**vertical tear-line.png** | source code in [text markup](/omr/net/txt-markup/)
**vertical tear-line.txt** | vertical tear line image
**vertical tear-line-recognized.png** | filled form
