---
title: Score elements description
type: docs
weight: 10
url: /net/template-generation/json/elements-description/score
---

## **Introduction**
Template generation markup supports several types of elements, and most elements have a number of options that define the element' properties and appearance. This allows creating functional and nice-looking custom templates for any of your needs i.e. surveys, answer sheets, tests - anything you need.

In this article, we provide a detailed description of score elements and its attributes with the usage examples represented in json markup.
Score element used for drawing table structure e.g. rows and columns.
Inside table structure positioned bubbles with score's attached to each one.
Upon filling bubble score is added to group score and question score.

## **ScoreGroup element**
The ScoreGroup element identified by field **"element_type"** and it's value **"ScoreGroup"**.
Can be used for grouping ScoreQuestion into logic sections. Supports ScoreQuestion elements as children.
Upon recognition return total amount of each ScoreQuestion summarized.

### **Attributes**
ScoreGroup element can be customized with attribute.

|**Attribute**|**Attribute Description**|**Required/Optional**|**Attribute Default Value**|**Attribute Usage Example**
| :- | :- | :- | :- | :- |
|name|Name of ScoreGroup|Optional|-|"name":"Hotel guest survey"
|element_type|Type of JSON object| Required|-| "element_type":"ScoreGroup"
|children|Array of other elements nested in this container|Required|-|see examples below
|score_type_table|Describe a display structure for each element inside it|Optional|table|"score_type_table":"table"|

## **ScoreQuestion element**
The ScoreGroup element identified by field **"element_type"** and it's value **"ScoreQuestion"**.
Represent question with multiple answers. Each answer holding a specific amount of value(score).
Upon recognition returns summarized value of each selected ScoreAnswer.
Grouping element. Support ScoreHeader and ScoreAnswer as child elements.
In table type ScoreHeader describe column header and ScoreAnswer row.

### **Attributes**
ScoreQuestion element can be customized with attributes.

|**Attribute**|**Attribute Description**|**Required/Optional**|**Attribute Default Value**|**Attribute Usage Example**|
| :- | :- | :- | :- | :- |
|name|Name of ScoreQuestion|Required|-|"name":"Are you satisfied with services provided?"
|element_type|Type of JSON object| Required|-| "element_type":"ScoreQuestion"
|children|Array of other elements nested in this container|Required|-|see examples below
|row_proportions|In table structure represent amount of width for each column in percent. Total value must be 100%. Amount of column must be equal to ScoreHeader children + 1(ScoreAnswer)|Required|-|"row_proportions": [80,10,10]|
|font_family|The font family of the text|Optional|Segoe UI|"font_family":"arial"|
|font_style|The style of the content|Optional|FontStyle.Regular|"font_style":"bold"|
|font_size|The size of the text content|Optional|12|"font_size":"16"|


## **ScoreHeader element**
The ScoreHeader element identified by field **"element_type"** and it's value **"ScoreHeader"**.
Can only be positioned inside of ScoreQuestion element as child.
In table structure represent column header of the table and content inside them.
**Amount of ScoreHeader inside must be equal to row_proportions property of ScoreQuestion element**
Based on type bubbles inside this column will either add Score to ScoreQuestion or display Score amount or do nothing.
**If you don't want to display Score amount for each answer you must omit ScoreHeader=Amount. It will affect only displaying. Recognition will summarize Score still.**

### **Attributes**
ScoreHeader element can be customized with attributes.
|**Attribute**|**Attribute Description**|**Required/Optional**|**Attribute Default Value**|**Attribute Usage Example**|
| :- | :- | :- | :- | :- |
|name|Name of ScoreHeader|Required|-|"name":"Yes"
|element_type|Type of JSON object| Required|-| "element_type":"ScoreHeader"
|header_type|Set content behavior inside this column <p>Positive = Value will be added upon bubble filling. </p> <p>Amount = Only displaying of value. </p> <p>Negative = upon filling value will not be added</p>|Required|Positive|<p>"score_header_type":"amount"</p><p>"score_header_type":"positive"</p><p>"score_header_type":"negative"</p>


## **ScoreAnswer element**
The ScoreHeader element identified by field **"element_type"** and it's value **"ScoreAnswer"**.
Can only be positioned inside of ScoreQuestion element as child.
Represent one of question answer and score value behind it

### **Attributes**
ScoreAnswer element can be customized with attributes.

|**Attribute**|**Attribute Description**|**Required/Optional**|**Attribute Default Value**|**Attribute Usage Example**|
| :- | :- | :- | :- | :- |
|score|number value that will be added to total sum of ScoreQuestion|Required|-|"score":5
|font_family|The font family of the content|Optional|Segoe UI|"font_family":"Arial"|
|font_style|The style of the content|Optional|FontStyle.Regular|"font_style":"Bold"|
|font_size|The size of the text content|Optional|12|"font_size":16|
|align|type of horizontal alignment for this text inside it's cell|Optional|left|<p>"align":"left"</p><p>"align":"right"</p><p>"align":"center"</p>



### **Example of ScoreGroup structure**
```json
{
    "children": [{
            "children": [{
                    "name": "Are you enjoying your stay in our Hotel?",
                    "font_family": "Segoe UI",
                    "font_style": "Bold",
                    "font_size": 20,
                    "align": "Center",
                    "element_type": "Text"
                }, {
                    "element_type": "EmptyLine"
                }, {
                    "element_type": "EmptyLine"
                }, {
                    "name": "main_container",
                    "children": [{
                            "name": "main_block",
                            "children": [{
                                    "name": "product survey",
                                    "children": [{
                                            "font_family": "Segoe UI",
                                            "font_style": "Bold",
                                            "font_size": 14,
                                            "row_proportions": [
                                                80,
                                                10,
                                                10
                                            ],
                                            "name": "How would you rate our hospitality?",
                                            "children": [{
                                                    "name": "Yes",
                                                    "header_type": "Positive",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "name": "No",
                                                    "header_type": "Negative",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "Score": 1,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "Website provided me with all information needed for booking.",
                                                }, {
                                                    "Score": 1,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "Location of hotel is excellent.",
                                                }, {
                                                    "Score": 5,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "Personnel is polite.",
                                                }, {
                                                    "Score": 1,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "I received a list of hotel amenities.",
                                                }
                                            ],
                                            "element_type": "ScoreQuestion"
                                        }, {
                                            "font_family": "Segoe UI",
                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "row_proportions": [
                                                80,
                                                10,
                                                10
                                            ],
                                            "name": "How would you rate our services ?",
                                            "children": [{
                                                    "name": "Yes",
                                                    "header_type": "Positive",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "name": "No",
                                                    "header_type": "Negative",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "Score": 2,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "Housekeeping visited my room daily.",
                                                }, {
                                                    "Score": 2,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "WiFi was fast and easy to connect.",
                                                }, {
                                                    "Score": 3,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "I enjoy continental Breakfast.",
                                                }, {
                                                    "Score": 3,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "I enjoy interior design of my hotel room.",
                                                }, {
                                                    "Score": 3,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "Air conditioner provided an optimal microclimate in my hotel room.",
                                                }
                                            ],
                                            "element_type": "ScoreQuestion"
                                        }, {
                                            "font_family": "Segoe UI",
                                            "font_style": "Bold",
                                            "font_size": 12,
                                            "row_proportions": [
                                                60,
                                                20,
                                                10,
                                                10
                                            ],
                                            "name": "How would you rate you total experience?",
                                            "children": [{
                                                    "name": "Score",
                                                    "header_type": "Amount",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "name": "Yes",
                                                    "header_type": "Positive",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "name": "No",
                                                    "header_type": "Negative",
                                                    "element_type": "ScoreHeader"
                                                }, {
                                                    "Score": 5,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "I enjoy my stay.",
                                                }, {
                                                    "Score": 10,
                                                    "element_type": "ScoreAnswer",
                                                    "name": "I will recommend it to my friends.",
                                                }
                                            ],
                                            "element_type": "ScoreQuestion"
                                        }
                                    ],
                                    "score_group_type": "Table",
                                    "element_type": "ScoreGroup"
                                }
                            ],
                            "column": 1,
                            "element_type": "Block"
                        }
                    ],
                    "columns_count": 1,
                    "element_type": "Container"
                }
            ],
            "element_type": "Page"
        }
    ],
    "element_type": "Template"
}

````

**Result**

**![todo:image_alt_text](hotel-survey-generation-result.png)**

**Inserted values**

**![todo:image_alt_text](hotel-survey-filled.png)**

**Recognition result (.csv)**

```text
Element Name,Value,
How would you rate our hospitality?,"Location of hotel is excellent.,Personnel is polite."
How would you rate our hospitality?_total,"6"
How would you rate our services ?,"Housekeeping visited my room daily.,I enjoy continental Breakfast.,I enjoy interior design of my hotel room."
How would you rate our services ?_total,"8"
How would you rate you total experience?,"I enjoy my stay.,I will recommend it to my friends."
How would you rate you total experience?_total,"15"
hotel guest survey,"29"

```