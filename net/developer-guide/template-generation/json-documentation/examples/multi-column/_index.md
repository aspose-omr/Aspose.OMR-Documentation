---
title: Multi-Column OMR Template example
type: docs
weight: 10
url: /net/template-generation/json/examples/multi-column
---

## **Introduction**
In this article, we provide example of creating a multi-column questionnaire.

### **Example for creating multi-column questionnaire**
<details>
<summary>Click to expand json markup</summary>

````json
{
    "children": [{
            "children": [{
                    "name": "1-st",
                    "children": [{
                            "name": "Process",
                            "children": [{
                                    "name": "Process",
                                    "children": [{
                                            "name": "Aspose Pty Ltd",
                                            "font_style": "Bold",
                                            "font_size": 8,
                                            "type": "Content"
                                        }, {
                                            "name": "Can Aspose.OMR process not only scans, but also photos?",
                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "type": "Content"
                                        }, {
                                            "name": "?hoose 1",
                                            "font_style": "Regular",
                                            "font_size": 9,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }, {
                                    "name": "Can Aspose.OMR process not only scans, but also photos?",
                                    "children": [{
                                            "name": "Yes",
                                            "children": [{
                                                    "name": "Yes",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "No",
                                            "children": [{
                                                    "name": "No",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }
                                    ],
                                    "type": "VerticalChoiceBox"
                                }
                            ],
                            "column": 1,
                            "border": "Square",
                            "border_size": 5,
                            "border_color": "Black",
                            "type": "Block"
                        }, {
                            "name": "Rate",
                            "children": [{
                                    "name": "Rate",
                                    "children": [{
                                            "name": "Aspose Pty Ltd",

                                            "font_style": "Bold",
                                            "font_size": 8,
                                            "type": "Content"
                                        }, {
                                            "name": "How would you rate the quiality of the product?",

                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "type": "Content"
                                        }, {
                                            "name": "?hoose 1",

                                            "font_style": "Regular",
                                            "font_size": 9,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }, {
                                    "name": "How would you rate the quiality of the product:",
                                    "children": [{
                                            "name": "5",
                                            "children": [{
                                                    "name": "Very high quality",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }, {
                                                    "name": "of the product",

                                                    "font_style": "Regular",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "4",
                                            "children": [{
                                                    "name": "High quality",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }, {
                                                    "name": "of the product",

                                                    "font_style": "Regular",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "3",
                                            "children": [{
                                                    "name": "Average quality",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }, {
                                                    "name": "of the product",

                                                    "font_style": "Regular",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }
                                    ],
                                    "type": "VerticalChoiceBox"
                                }
                            ],
                            "column": 2,
                            "border": "Square",
                            "border_size": 5,
                            "border_color": "Black",
                            "type": "Block"
                        }, {
                            "name": "Forms",
                            "children": [{
                                    "name": "Forms",
                                    "children": [{
                                            "name": "Aspose Pty Ltd",

                                            "font_style": "Bold",
                                            "font_size": 8,
                                            "type": "Content"
                                        }, {
                                            "name": "Aspose.OMR works with any kind of OMR forms: tests, exams, questionnaires, surveys, etc.?",

                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "type": "Content"
                                        }, {
                                            "name": "?hoose 1",

                                            "font_style": "Regular",
                                            "font_size": 9,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }, {
                                    "name": "Aspose.OMR works with any kind of OMR forms: tests, exams, questionnaires, surveys, etc.?",
                                    "children": [{
                                            "name": "Yes",
                                            "children": [{
                                                    "name": "Yes, indeed!",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "No",
                                            "children": [{
                                                    "name": "No",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }
                                    ],
                                    "type": "VerticalChoiceBox"
                                }
                            ],
                            "column": 1,
                            "border": "Square",
                            "border_size": 5,
                            "border_color": "Black",
                            "type": "Block"
                        }, {
                            "name": "Reccomend",
                            "children": [{
                                    "name": "Reccomend",
                                    "children": [{
                                            "name": "Aspose Pty Ltd",

                                            "font_style": "Bold",
                                            "font_size": 8,
                                            "type": "Content"
                                        }, {
                                            "name": "How likely is it that you would reccomend our company to a friend or colleague?",

                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "type": "Content"
                                        }, {
                                            "name": "?hoose 1",

                                            "font_style": "Regular",
                                            "font_size": 9,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }, {
                                    "name": "How likely is it that you would reccomend our company to a friend or colleague?",
                                    "children": [{
                                            "name": "1",
                                            "children": [{
                                                    "name": "1",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "2",
                                            "children": [{
                                                    "name": "2",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "3",
                                            "children": [{
                                                    "name": "3",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "4",
                                            "children": [{
                                                    "name": "4",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "5",
                                            "children": [{
                                                    "name": "5",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "6",
                                            "children": [{
                                                    "name": "6",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "7",
                                            "children": [{
                                                    "name": "7",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "8",
                                            "children": [{
                                                    "name": "8",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }, {
                                            "name": "9",
                                            "children": [{
                                                    "name": "9",

                                                    "font_style": "Bold",
                                                    "font_size": 10,
                                                    "type": "Content"
                                                }
                                            ],
                                            "type": "Answer"
                                        }
                                    ],
                                    "type": "VerticalChoiceBox"
                                }
                            ],
                            "column": 3,
                            "border": "Square",
                            "border_size": 5,
                            "border_color": "Black",
                            "type": "Block"
                        }
                    ],
                    "columns_count": 3,
                    "container_type": "Normal",
                    "type": "Container"
                }, {

                    "type": "EmptyLine"
                }, {
                    "name": "Test4",
                    "value": "Aspose Pty Ltd",
                    "barcode_type": "qr",
                    "qr_version": "Auto",
                    "align": "Center",
                    "height": 250,
                    "codetext": true,
                    "X": 2100,
                    "Y": 3030,
                    "type": "Barcode"
                }, {
                    "name": "Footer",
                    "children": [{
                            "name": "1",
                            "children": [{
                                    "name": "1",
                                    "children": [{
                                            "name": "Precinct Aspose Style 1",

                                            "font_style": "Bold",
                                            "font_size": 14,
                                            "type": "Content"
                                        }, {
                                            "name": "� Aspose Pty Ltd 2001-2021",

                                            "font_style": "Regular",
                                            "font_size": 10,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }
                            ],
                            "column": 1,
                            "border": "None",
                            "border_size": 3,
                            "border_color": "Black",
                            "type": "Block"
                        }, {
                            "name": "2",
                            "children": [{
                                    "name": "2",
                                    "children": [{
                                            "name": "All Rights Reserved",

                                            "font_style": "Regular",
                                            "font_size": 10,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }
                            ],
                            "column": 2,
                            "border": "None",
                            "border_size": 3,
                            "border_color": "Black",
                            "type": "Block"
                        }, {
                            "name": "3",
                            "children": [{
                                    "name": "3",
                                    "children": [{
                                            "name": "Page 1",

                                            "font_style": "Bold",
                                            "font_size": 14,
                                            "type": "Content"
                                        }, {
                                            "name": "June 26, 2021",

                                            "font_style": "Regular",
                                            "font_size": 10,
                                            "type": "Content"
                                        }
                                    ],
                                    "paragraph_type": "Normal",
                                    "type": "Paragraph"
                                }
                            ],
                            "column": 3,
                            "border": "None",
                            "border_size": 3,
                            "border_color": "Black",
                            "type": "Block"
                        }
                    ],
                    "columns_count": 3,
                    "container_type": "Footer",
                    "type": "Container"
                }
            ],
            "type": "Page"
        }
    ],
    "type": "Template"
}

````
</details>


**Result**

**![todo:image_alt_text](multi-column-template-template.png)**



