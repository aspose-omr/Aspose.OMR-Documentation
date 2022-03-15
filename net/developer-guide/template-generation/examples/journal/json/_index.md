---
title: Medical Journal questionnaire (.json)
type: docs
weight: 5
url: /net/template-generation/examples/journal/json
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
var configPath = @"C:\Users\User\Desktop\template\template.json";

var result = engine.GenerateJSONTemplate(configPath, settings);
result.Save(@"C:\Users\User\Desktop\template", "generated_template");
````

</details>




**Template JSON markdown**

<details>
<summary>JSON markdown</summary>

```json
{
  "name": null,
  "children": [
    {
      "name": null,
      "children": [
        {
          "name": "Neural Questionnaire\r\n",
          "font_family": "Segoe UI",
          "font_style": "Bold",
          "font_size": 16,
          "align": "Left",
          "element_type": "Text"
        },
        {
          "name": "______________________________________________________________________________________________________________________________\r\n",
          "font_family": "Segoe UI",
          "font_style": "Regular",
          "font_size": 9,
          "align": "Left",
          "element_type": "Text"
        },
        {
          "name": "",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "Your comments are important to us. This form provides you with the opportunity to express your opinions. Our goal is to make Neural Today your source for practical and clinical neuropsychiatric information. By filling out this Questionnaire, you enable us to incorporate your views about our editorial content in future issues. Please fill out this form in its entirety. Thank you.",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 10,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 1,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "personal info",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "______________________________________________________________________________________________________________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "Name (please print)",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "",
                  "height": 40,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "______________________________________________________________________________________________________________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "Address",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                }
              ],
              "column": 1,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": true,
              "element_type": "Block"
            }
          ],
          "columns_count": 1,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "______________________________________________________________________________________________________________________________\r\n",
          "font_family": "Segoe UI",
          "font_style": "Regular",
          "font_size": 9,
          "align": "Left",
          "element_type": "Text"
        },
        {
          "name": "",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "City",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
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
              "name": "",
              "children": [
                {
                  "name": "State",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "",
              "children": [
                {
                  "name": "Zip Code",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
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
              "name": "______________________________________________________________________________________________________________________________\r\n",
              "font_family": "Segoe UI",
              "font_style": "Regular",
              "font_size": 9,
              "align": "Left",
              "element_type": "Text"
            },
            {
              "name": "",
              "children": [
                {
                  "name": "E-mail",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
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
              "name": "",
              "children": [
                {
                  "name": "Specialty",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 0,
          "columns_proportions": [
            33,
            33,
            34
          ],
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "______________________________________________________________________________________________________________________________\r\n",
          "font_family": "Segoe UI",
          "font_style": "Regular",
          "font_size": 9,
          "align": "Left",
          "element_type": "Text"
        },
        {
          "name": "",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "Signature",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
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
              "name": "",
              "children": [
                {
                  "name": "Date",
                  "font_family": "Segoe UI",
                  "font_style": "Italic",
                  "font_size": 8,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 0,
          "columns_proportions": [
            33,
            33,
            34
          ],
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "",
          "children": [
            {
              "name": "1",
              "children": [
                {
                  "name": "Fax this form to 123-321-0800. Or mail it to: Neural Today, ZTX Communications, Inc., 111 Fifth Street, 2th Floor, New York, NY 15",
                  "font_family": "Segoe UI",
                  "font_style": "Bold",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                }
              ],
              "column": 1,
              "border": "Square",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 1,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "two_columns",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "1. On scale of 1 to 5 (1=Poor, 5=Excellent), please indicate your level of interest and/or satisfaction with the editorial content in this issue.",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 10,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "",
                  "height": 30,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "Original Research Articles",
                  "font_family": "Segoe UI",
                  "font_style": [
                    "Bold",
                    "Underline"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "Personality Disorders",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "hide_name": true,
                  "name": "Personality Disorders",
                  "orientation": "Horizontal",
                  "bubble_size": "Extrasmall",
                  "threshold": 3,
                  "element_type": "CheckBox",
                  "children": [
                    {
                      "name": "1",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "2",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "3",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "4",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "5",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    }
                  ],
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9
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
              "name": "",
              "children": [
                {
                  "name": "",
                  "height": 30,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "Departments",
                  "font_family": "Segoe UI",
                  "font_style": [
                    "Bold",
                    "Underline"
                  ],
                  "font_size": 12,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "Clinical Updates in Neuropsychiatry",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "hide_name": true,
                  "name": "Clinical Updates in Neuropsychiatry",
                  "orientation": "Horizontal",
                  "bubble_size": "Extrasmall",
                  "threshold": 3,
                  "element_type": "CheckBox",
                  "children": [
                    {
                      "name": "1",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "2",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "3",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "4",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "5",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    }
                  ],
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9
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
              "name": "",
              "children": [
                {
                  "name": "From the Editor's Desk",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "hide_name": true,
                  "name": "From the Editor's Desk",
                  "orientation": "Horizontal",
                  "bubble_size": "Extrasmall",
                  "threshold": 3,
                  "element_type": "CheckBox",
                  "children": [
                    {
                      "name": "1",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "2",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "3",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "4",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "5",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    }
                  ],
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9
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
              "name": "",
              "children": [
                {
                  "name": "CME",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "hide_name": true,
                  "name": "CME",
                  "orientation": "Horizontal",
                  "bubble_size": "Extrasmall",
                  "threshold": 3,
                  "element_type": "CheckBox",
                  "children": [
                    {
                      "name": "1",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "2",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "3",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "4",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "5",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    }
                  ],
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9
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
              "name": "",
              "children": [
                {
                  "name": "2. Which areas of neuropsychiatry would you like us to cover on the future?",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
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
              "name": "3.",
              "children": [
                {
                  "name": "3. Please describe your reading pattern for this issue:\t",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "reading pattern",
                  "children": [
                    {
                      "name": "Read cover to cover",
                      "children": [
                        {
                          "name": "Read cover to cover",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Skimmed table of contents",
                      "children": [
                        {
                          "name": "Skimmed table of contents",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Read select items of interest",
                      "children": [
                        {
                          "name": "Read select items of interest",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Skimmed text",
                      "children": [
                        {
                          "name": "Skimmed text",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Did not read",
                      "children": [
                        {
                          "name": "Did not read",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    }
                  ],
                  "element_type": "VerticalChoiceBox"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "4.",
              "children": [
                {
                  "name": "4. On a scale of 1 to 5(1=Incomplete, 5=Comperehensive), how would you describe the depth of coverage for this issue?",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "hide_name": true,
                  "name": "4.",
                  "orientation": "Horizontal",
                  "bubble_size": "Extrasmall",
                  "threshold": 3,
                  "element_type": "CheckBox",
                  "children": [
                    {
                      "name": "1",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "2",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "3",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "4",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    },
                    {
                      "name": "5",
                      "font_family": "Segoe UI",
                      "font_style": "Regular",
                      "font_size": 9,
                      "content_type": "Normal",
                      "align": "Left",
                      "element_type": "Content"
                    }
                  ],
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "",
              "height": 20,
              "element_type": "EmptyLine"
            },
            {
              "name": "",
              "children": [
                {
                  "name": "5. Any other comments about Neural Today editorial content, design, or overall, overall usefulness?",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "____________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "",
              "children": [
                {
                  "name": "6. Please indicate your title:",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "title",
                  "children": [
                    {
                      "name": "Psychiatrist",
                      "children": [
                        {
                          "name": "Psychiatrist",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Neurologist",
                      "children": [
                        {
                          "name": "Neurologist",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 10,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    }
                  ],
                  "element_type": "VerticalChoiceBox"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            }
          ],
          "columns_count": 2,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "",
          "height": 250,
          "element_type": "EmptyLine"
        },
        {
          "name": "______________________________________________________________________________________________________________________________\r\n",
          "font_family": "Segoe UI",
          "font_style": "Regular",
          "font_size": 9,
          "align": "Left",
          "element_type": "Text"
        },
        {
          "name": "footer",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "Volume 8 - Number 10",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
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
              "name": "",
              "children": [
                {
                  "name": "777",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                }
              ],
              "column": 2,
              "border": "None",
              "border_size": 3,
              "border_color": "Black",
              "is_clipped": false,
              "element_type": "Block"
            },
            {
              "name": "",
              "children": [
                {
                  "name": "Neural Today - October 2003",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Right",
                  "element_type": "Content"
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
          "columns_count": 3,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        }
      ],
      "element_type": "Page"
    }
  ],
  "element_type": "Template"
}
```

</details>

**Template result**

**![todo:image_alt_text](journal-json.png)**