---
weight: 20
date: "2022-06-03"
author: "Vladimir Lapin"
type: docs
url: /net/showcases/satisfaction/grouped/
title: Customer satisfaction survey with grouped layout
description: OMR ready customer satisfaction survey with grouped layout
keywords:
- examples
- branding
- survey
- source
- survey
- satisfaction
---

Understand how your clients are satisfied with your services, capabilities and their customer journey.

![OMR ready customer satisfaction survey with grouped layout template](car-dealership.png)

## Source code

<details>
<summary>Text markup</summary>

```
?text=AmazeCar Customer Satisfaction Survey
	font_style=bold
	font_size=18
	align=center
?image=logo.jpg
	width=200
	height=200
	align=left
	y=100
	x=278
?container=description
	columns_count=1
?block=
	column=1
?empty_line=
	height=50
?content=Thank you for your purchase! We want your experience to be Perfect! Please help us be more Amazing by answering some question about your purchase.
	font_style=Italic
&block
&container
?container=about yourself_header
	columns_proportions=100%
	block_bottom_margin=0
	block_top_padding=0
?block=
	column=1
	border=none
?content=Please tell us a bit about yourself...
	font_style=bold
	font_size=14
	align=center
&block
&container
?empty_line=
	height=25
?container=about yourself_content
	columns_count=3
	block_bottom_margin=0
	block_top_padding=0
	block_right_margin=0
?block=
	column=1
	border=square
?content=Gender:
	font_style=bold
	font_size=12
?vertical_choicebox=Gender
?answer=Female
?content=Female
&answer
?answer=Male
?content=Male
&answer
?answer=Other(specify)
?content=Other(specify)
?write_in=Gender
&answer
&vertical_choicebox
?empty_line=
	height=85
&block
?block=
	column=2
	border=square
?content=Age Group:
	font_style=bold
	font_size=12
?vertical_choicebox=Age Group
?answer=18-21
?content=18-21
&answer
?answer=21-30
?content=21-30
&answer
?answer=31-45
?content=31-45
&answer
?answer=46-60
?content=46-60
&answer
?answer=>60
?content=>60
&answer
?answer=21-30
?content=21-30
&answer
&vertical_choicebox
?empty_line=
	height=23
&block
?block=
	column=3
	border=square
?content=Income Level:
	font_style=bold
	font_size=12
?vertical_choicebox=Gender
?answer=<$50K
?content=<$50K
&answer
?answer=$50-$100K
?content=$50-$100K
&answer
?answer=$100-$150K
?content=$100-$150K
&answer
?answer=>$150K
?content=>$150K
&answer
&vertical_choicebox
?empty_line=
	height=167
&block
&container
?empty_line=
	height=100
?container=salesperson_header
	columns_count=1
	block_bottom_margin=0
	block_top_padding=0
?block=
	column=1
	border=none
?content=Please rate your SALESPERSON on the following
	font_style=bold
	font_size=12
	align=center
?empty_line=
	height=25
&block
&container
?container=salesperson_content
	columns_count=4
	block_bottom_margin=0
	block_top_padding=0
	block_right_margin=0
?block=
	column=1
	border=square
?content=The manner in which you were greeted
	font_style=bold
	font_size=10
?vertical_choicebox=The manner in which you were greeted
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=50
&block
?block=
	column=2
	border=square
?content=Sincerity and honesty in dealing with you
	font_style=bold
	font_size=10
?vertical_choicebox=Sincerity and honesty in dealing with you
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=50
&block
?block=
	column=3
	border=square
?content=Consideration of your time
	font_style=bold
	font_size=10
?vertical_choicebox=Consideration of your time
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=92
&block
?block=
	column=4
	border=square
?content=Ability to listen, understand and answer your questions
	font_style=bold
	font_size=10
?vertical_choicebox=Ability to listen, understand and answer your questions
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=50
&block
&container
?empty_line=
	height=100
?container=salesteam_header
	columns_count=1
	block_bottom_margin=0
	block_top_padding=0
?block=
	column=1
	border=none
?content=Please rate our SALES TEAM on the following
	font_style=bold
	font_size=12
	align=center
?empty_line=
	height=25
&block
&container
?container=salesteam_content
	columns_count=4
	block_bottom_margin=0
	block_top_padding=0
	block_right_margin=0
?block=
	column=1
	border=square
?content=The vehicle price and/or payments were discussed in a thorough manner
	font_style=bold
	font_size=10
?vertical_choicebox=The vehicle price and/or payments were discussed in a thorough manner
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=50
&block
?block=
	column=2
	border=square
?content=Explanation of warranty coverage
	font_style=bold
	font_size=10
?vertical_choicebox=Explanation of warranty coverage
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=92
&block
?block=
	column=3
	border=square
?content=The professional manner in which you were treated
	font_style=bold
	font_size=10
?vertical_choicebox=The professional manner in which you were treated
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=92
&block
?block=
	column=4
	border=square
?content=Fulfilled all commitments made to you
	font_style=bold
	font_size=10
?vertical_choicebox=Fulfilled all commitments made to you
?answer=Fantastic!
?content=Fantastic!
&answer
?answer=Excellent
?content=Excellent
&answer
?answer=Satisfactory
?content=Satisfactory
&answer
?answer=Mediocre
?content=Mediocre
&answer
?answer=Negative
?content=Negative
&answer
&vertical_choicebox
?empty_line=
	height=92
&block
&container
?container=other_header
	columns_count=1
	block_bottom_margin=0
	block_top_padding=0
?block=
	column=1
	border=none
?empty_line=
	height=25
?content=More about the buying experience
	font_style=bold
	font_size=12
	align=center
?empty_line=
	height=25
&block
&container
#If you have contacted out store by phone, how satisfied are you with the way your call was handled?
	()Fantastic! ()Excellent ()Satisfactory ()Mediocre ()Negative
?container=
	columns_count=1
?block=
	column=1	
?content=If you overall experience was unsatisfactory - leave your contact information. We'll make it up to you!
?empty_line=
	height=25
?write_in=contact_information
&block
&container
?barcode=test_id
	codetext=true
	value=15478977
	barcode_type=Code32
```

</details>

<details>
<summary>JSON markup</summary>

```json
{
    "children": [{
            "children": [{
                    "name": "AmazeCar Customer Satisfaction Survey",
                    "font_style": "Bold",
                    "font_size": 18,
                    "align": "Center",
                    "element_type": "Text"
                }, {
                    "align": "Left",
                    "name": "logo.jpg",
                    "x": 278,
                    "y": 100,
                    "height": 200,
                    "width": 200,
                    "element_type": "Image"
                }, {
                    "name": "description",
                    "children": [{
                            "children": [{
                                    "height": 50,
                                    "element_type": "EmptyLine"
                                }, {
                                    "name": "Thank you for your purchase! We want your experience to be Perfect! Please help us be more Amazing by answering some question about your purchase.",
                                    "font_style": "Italic",
                                    "align": "Left",
                                    "element_type": "Content"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "container_type": "Normal",
                    "element_type": "Container"
                }, {
                    "name": "about yourself_header",
                    "children": [{
                            "children": [{
                                    "name": "Please tell us a bit about yourself...",
                                    "font_style": "Bold",
                                    "font_size": 14,
                                    "align": "Center",
                                    "element_type": "Content"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_proportions": [
                        100
                    ],
                    "container_type": "Normal",
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "height": 25,
                    "element_type": "EmptyLine"
                }, {
                    "name": "about yourself_content",
                    "children": [{
                            "children": [{
                                    "name": "Gender:",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Gender",
                                    "children": [{
                                            "name": "Female",
                                            "children": [{
                                                    "name": "Female",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Male",
                                            "children": [{
                                                    "name": "Male",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Other(specify)",
                                            "children": [{
                                                    "name": "Other(specify)",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }, {
                                                    "name": "Gender",
                                                    "element_type": "WriteIn"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 85,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Age Group:",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Age Group",
                                    "children": [{
                                            "name": "18-21",
                                            "children": [{
                                                    "name": "18-21",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "21-30",
                                            "children": [{
                                                    "name": "21-30",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "31-45",
                                            "children": [{
                                                    "name": "31-45",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "46-60",
                                            "children": [{
                                                    "name": "46-60",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": ">60",
                                            "children": [{
                                                    "name": ">60",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "21-30",
                                            "children": [{
                                                    "name": "21-30",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 23,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 2,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Income Level:",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Gender",
                                    "children": [{
                                            "name": "<$50K",
                                            "children": [{
                                                    "name": "<$50K",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "$50-$100K",
                                            "children": [{
                                                    "name": "$50-$100K",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "$100-$150K",
                                            "children": [{
                                                    "name": "$100-$150K",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": ">$150K",
                                            "children": [{
                                                    "name": ">$150K",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 167,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 3,
                            "border": "Square",
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 3,
                    "container_type": "Normal",
                    "block_right_margin": 0,
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "height": 100,
                    "element_type": "EmptyLine"
                }, {
                    "name": "salesperson_header",
                    "children": [{
                            "children": [{
                                    "name": "Please rate your SALESPERSON on the following",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Center",
                                    "element_type": "Content"
                                }, {
                                    "height": 25,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "container_type": "Normal",
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "name": "salesperson_content",
                    "children": [{
                            "children": [{
                                    "name": "The manner in which you were greeted",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "The manner in which you were greeted",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 50,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Sincerity and honesty in dealing with you",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Sincerity and honesty in dealing with you",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 50,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 2,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Consideration of your time",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Consideration of your time",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 92,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 3,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Ability to listen, understand and answer your questions",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Ability to listen, understand and answer your questions",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 50,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 4,
                            "border": "Square",
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 4,
                    "container_type": "Normal",
                    "block_right_margin": 0,
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "height": 100,
                    "element_type": "EmptyLine"
                }, {
                    "name": "salesteam_header",
                    "children": [{
                            "children": [{
                                    "name": "Please rate our SALES TEAM on the following",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Center",
                                    "element_type": "Content"
                                }, {
                                    "height": 25,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "container_type": "Normal",
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "name": "salesteam_content",
                    "children": [{
                            "children": [{
                                    "name": "The vehicle price and/or payments were discussed in a thorough manner",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "The vehicle price and/or payments were discussed in a thorough manner",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 50,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Explanation of warranty coverage",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Explanation of warranty coverage",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 92,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 2,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "The professional manner in which you were treated",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "The professional manner in which you were treated",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 92,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 3,
                            "border": "Square",
                            "element_type": "Block"
                        }, {
                            "children": [{
                                    "name": "Fulfilled all commitments made to you",
                                    "font_style": "Bold",
                                    "font_size": 10,
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "name": "Fulfilled all commitments made to you",
                                    "children": [{
                                            "name": "Fantastic!",
                                            "children": [{
                                                    "name": "Fantastic!",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Excellent",
                                            "children": [{
                                                    "name": "Excellent",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Satisfactory",
                                            "children": [{
                                                    "name": "Satisfactory",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Mediocre",
                                            "children": [{
                                                    "name": "Mediocre",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }, {
                                            "name": "Negative",
                                            "children": [{
                                                    "name": "Negative",
                                                    "align": "Left",
                                                    "element_type": "Content"
                                                }
                                            ],
                                            "bubble_type": "Round",
                                            "element_type": "Answer"
                                        }
                                    ],
                                    "element_type": "VerticalChoiceBox",
                                    "top_padding": 0
                                }, {
                                    "height": 92,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 4,
                            "border": "Square",
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 4,
                    "container_type": "Normal",
                    "block_right_margin": 0,
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "name": "other_header",
                    "children": [{
                            "children": [{
                                    "height": 25,
                                    "element_type": "EmptyLine"
                                }, {
                                    "name": "More about the buying experience",
                                    "font_style": "Bold",
                                    "font_size": 12,
                                    "align": "Center",
                                    "element_type": "Content"
                                }, {
                                    "height": 25,
                                    "element_type": "EmptyLine"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "container_type": "Normal",
                    "block_bottom_margin": 0,
                    "block_top_padding": 0,
                    "element_type": "Container"
                }, {
                    "align": "Left",
                    "answers_string": "\t()Fantastic! ()Excellent ()Satisfactory ()Mediocre ()Negative",
                    "question_text": "If you have contacted out store by phone, how satisfied are you with the way your call was handled?",
                    "element_type": "ChoiceBox"
                }, {
                    "children": [{
                            "children": [{
                                    "name": "If you overall experience was unsatisfactory - leave your contact information. We'll make it up to you!",
                                    "align": "Left",
                                    "element_type": "Content"
                                }, {
                                    "height": 25,
                                    "element_type": "EmptyLine"
                                }, {
                                    "name": "contact_information",
                                    "element_type": "WriteIn"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "container_type": "Normal",
                    "element_type": "Container"
                }, {
                    "name": "test_id",
                    "value": "15478977",
                    "barcode_type": "code32",
                    "align": "Center",
                    "codetext": true,
                    "element_type": "Barcode"
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
    BubbleColor = Color.Black,
    BubbleSize = BubbleSize.Normal,
    FontStyle = FontStyle.Regular,
    FontSize = 10,
    FontFamily = "Calibri",
};
```

## Recognition results

![OMR ready customer satisfaction survey with grouped layout filled](car-dealership-recognized.png)

```
Element Name,Value,
Ability to listen, understand and answer your questions,"Excellent"
Age Group,"31-45"
Consideration of your time,"Satisfactory"
Explanation of warranty coverage,"Satisfactory"
Fulfilled all commitments made to you,"Fantastic!"
Gender,"Male"
Gender,"$100-$150K"
Question1,"C"
Sincerity and honesty in dealing with you,"Satisfactory"
test_id,"154789770"
The manner in which you were greeted,"Fantastic!"
The professional manner in which you were treated,"Satisfactory"
The vehicle price and/or payments were discussed in a thorough manner,"Fantastic!"
```

## Download

[Click here](https://github.com/aspose-omr/Aspose.OMR-Documentation/blob/master/net/showcases/download/satisfaction-grouped.zip) to download full template sources and related files. 

**Package structure:**

File | Description
---- | -----------
**car-dealership.csv** | recognition results based on the filled form available in this package
**car-dealership.json** | source code in [JSON markup](/omr/net/json-markup/)
**car-dealership.omr** | recognition pattern
**car-dealership.png** | printable form
**car-dealership.txt** | source code in [text markup](/omr/net/txt-markup/)
**car-dealership-recognized.png** | filled form
**logo.jpg** | company logo
**settings.txt** | [page settings](/omr/net/generate-template/page-setup/)
