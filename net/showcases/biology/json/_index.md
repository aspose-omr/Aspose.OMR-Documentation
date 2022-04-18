---
title: Biology test (.json)
type: docs
weight: 5
url: /net/showcases/biology/json
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
          "name": "header",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "",
                  "height": 200,
                  "element_type": "EmptyLine"
                },
                {
                  "name": "Biology test",
                  "font_family": "Segoe UI",
                  "font_style": "Bold",
                  "font_size": 14,
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
                  "name": "WHS",
                  "font_family": "Segoe UI",
                  "font_style": "Bold",
                  "font_size": 20,
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
              "name": "",
              "children": [
                {
                  "name": "West High School",
                  "font_family": "Segoe UI",
                  "font_style": "Bold",
                  "font_size": 10,
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
            }
          ],
          "columns_count": 3,
          "columns_proportions": null,
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "",
          "height": 150,
          "element_type": "EmptyLine"
        },
        {
          "name": "",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "__________________________________________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "students name",
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
                  "name": "______________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "class",
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
                  "name": "_______________",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Center",
                  "element_type": "Content"
                },
                {
                  "name": "date",
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
            }
          ],
          "columns_count": 0,
          "columns_proportions": [
            60,
            20,
            20
          ],
          "container_type": "Normal",
          "element_type": "Container"
        },
        {
          "name": "",
          "children": [
            {
              "name": "",
              "children": [
                {
                  "name": "1. Ordinary table salt is sodium chloride. What is baking soda?",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "1. Ordinary table salt is sodium chloride. What is baking soda?",
                  "children": [
                    {
                      "name": "Potassium chloride",
                      "children": [
                        {
                          "name": "Potassium chloride",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Potassium carbonate",
                      "children": [
                        {
                          "name": "Potassium carbonate",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Potassium hydroxide",
                      "children": [
                        {
                          "name": "Potassium hydroxide",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Sodium bicarbonate",
                      "children": [
                        {
                          "name": "Sodium bicarbonate",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
                  "name": "2. Ozone hole refers to",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "2. Ozone hole refers to",
                  "children": [
                    {
                      "name": "hole in ozone layer",
                      "children": [
                        {
                          "name": "hole in ozone layer",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "decrease in the ozone layer in troposphere",
                      "children": [
                        {
                          "name": "decrease in the ozone layer in troposphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "decrease in thickness of ozone layer in stratosphere",
                      "children": [
                        {
                          "name": "decrease in thickness of ozone layer in stratosphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "increase in the thickness of ozone layer in troposphere",
                      "children": [
                        {
                          "name": "increase in the thickness of ozone layer in troposphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
                  "name": "3. Pine, fir, spruce, cedar, larch and cypress are the famous timber-yielding plants of which several also occur widely in the hilly regions of India. All these belong to",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "3.",
                  "children": [
                    {
                      "name": "angiosperms",
                      "children": [
                        {
                          "name": "angiosperms",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "decrease in the ozone layer in troposphere",
                      "children": [
                        {
                          "name": "decrease in the ozone layer in troposphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "decrease in thickness of ozone layer in stratosphere",
                      "children": [
                        {
                          "name": "decrease in thickness of ozone layer in stratosphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "increase in the thickness of ozone layer in troposphere",
                      "children": [
                        {
                          "name": "increase in the thickness of ozone layer in troposphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
                  "name": "4. Pollination is best defined as",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "4.",
                  "children": [
                    {
                      "name": "transfer of pollen from anther to stigma",
                      "children": [
                        {
                          "name": "transfer of pollen from anther to stigma",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "germination of pollen grains",
                      "children": [
                        {
                          "name": "germination of pollen grains",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "growth of pollen tube in ovule",
                      "children": [
                        {
                          "name": "growth of pollen tube in ovule",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "visiting flowers by insects",
                      "children": [
                        {
                          "name": "visiting flowers by insects",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
                  "name": "5. Plants receive their nutrients mainly from",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "5.",
                  "children": [
                    {
                      "name": "chlorophyll",
                      "children": [
                        {
                          "name": "chlorophyll",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "atmosphere",
                      "children": [
                        {
                          "name": "atmosphere",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "light",
                      "children": [
                        {
                          "name": "light",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "soil",
                      "children": [
                        {
                          "name": "soil",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
                  "name": "6. Movement of cell against concentration gradient is called",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "6.",
                  "children": [
                    {
                      "name": "osmosis",
                      "children": [
                        {
                          "name": "osmosis",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "active transport",
                      "children": [
                        {
                          "name": "active transport",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "diffusion",
                      "children": [
                        {
                          "name": "diffusion",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "passive transport",
                      "children": [
                        {
                          "name": "passive transport",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
              "name": "",
              "children": [
                {
                  "name": "7. Photosynthesis generally takes place in which parts of the plant?",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "7.",
                  "children": [
                    {
                      "name": "Leaf and other chloroplast bearing parts",
                      "children": [
                        {
                          "name": "Leaf and other chloroplast bearing parts",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "stem and leaf",
                      "children": [
                        {
                          "name": "stem and leaf",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Roots and chloroplast bearing parts",
                      "children": [
                        {
                          "name": "Roots and chloroplast bearing parts",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "Bark and leaf",
                      "children": [
                        {
                          "name": "Bark and leaf",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
              "name": "",
              "children": [
                {
                  "name": "8. Most fish do not sink in water because of the presence of",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "I. swim bladder",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "II. air bladder",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "III. air sacs",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "IV. air in spongy bones",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "8.",
                  "children": [
                    {
                      "name": "I and II are correct",
                      "children": [
                        {
                          "name": "I and II are correct",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "II and III are correct",
                      "children": [
                        {
                          "name": "II and III are correct",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "III and IV are correct",
                      "children": [
                        {
                          "name": "III and IV are correct",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "I, II, III and IV are correct",
                      "children": [
                        {
                          "name": "I, II, III and IV are correct",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
              "name": "",
              "children": [
                {
                  "name": "9. Plants synthesis protein from",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "9.",
                  "children": [
                    {
                      "name": "starch",
                      "children": [
                        {
                          "name": "starch",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "sugar",
                      "children": [
                        {
                          "name": "sugar",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "amino acids",
                      "children": [
                        {
                          "name": "amino acids",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "fatty acids",
                      "children": [
                        {
                          "name": "fatty acids",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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
              "name": "",
              "children": [
                {
                  "name": "10. Plants absorb dissolved nitrates from soil and convert them into",
                  "font_family": "Segoe UI",
                  "font_style": "Regular",
                  "font_size": 9,
                  "content_type": "Normal",
                  "align": "Left",
                  "element_type": "Content"
                },
                {
                  "name": "9.",
                  "children": [
                    {
                      "name": "free nitrogen",
                      "children": [
                        {
                          "name": "free nitrogen",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "urea",
                      "children": [
                        {
                          "name": "urea",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "ammonia",
                      "children": [
                        {
                          "name": "ammonia",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
                          "content_type": "Normal",
                          "align": "Left",
                          "element_type": "Content"
                        }
                      ],
                      "element_type": "Answer"
                    },
                    {
                      "name": "proteins",
                      "children": [
                        {
                          "name": "proteins",
                          "font_family": "Segoe UI",
                          "font_style": "Regular",
                          "font_size": 9,
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

**![todo:image_alt_text](biology-json.png)**