---
weight: 40
date: "2024-05-13"
author: "Vladimir Lapin"
type: docs
url: /java/design-form/text/
title: Text
feedback: OMRJAVA
description: A markup element that adds a line of text to the form.
keywords:
- layout
- markup
- template
- design
- form
- text
- txt
---

This element is used to add one or more lines of text to the form.

## Syntax

The element declaration begins with `?text=` statement followed by a text to be displayed on the form, and continues until an empty line, another element declaration, or an attribute is found.

New lines following `?text=` declaration are treated as line breaks in the text.

{{% alert color="caution" %}} 
Never add a **tab character** before subsequent lines of text. Otherwise, they will be misinterpreted as attributes.
{{% /alert %}}

### Attributes

The **text** element can be customized by adding optional attributes to it.

An attribute is written as `[attribute_name]=[value]`. Each attribute must be placed on a **new line** immediately after the opening `?text=` statement or another attribute, and must begin with a **tab character**.

Attribute | Default value | Description | Usage example
--------- | ------------- | ----------- | -------------
**font_family** | Segoe UI | The font family for the text. | `font_family=Courier New`
**font_style** | regular | The font style for a text: `bold`, `italic` or `underline`. | `font_style=bold`
**font_size** | 12 | Font size for the text. | `font_size=16`
**font_color** | Black | Text color. Can be picked from one of the values listed [below](#supported-text-colors). | `font_color=red`
**align** | left | Horizontal text alignment: `left`, `center` or `right`. | `align=center`

{{% alert color="caution" %}} 
The selected font must be installed in the system that generates the printed form! Otherwise, form generation will fail with an exception.
{{% /alert %}}

#### Supported text colors

<table>
<tr><th>Color</th><th>Value</th></tr>
<tr><td>&nbsp;</td><td><code>undefined</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:AliceBlue;"></div></td><td><code>AliceBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:AntiqueWhite;"></div></td><td><code>AntiqueWhite</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Aqua;"></div></td><td><code>Aqua</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Aquamarine;"></div></td><td><code>Aquamarine</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Azure;"></div></td><td><code>Azure</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Beige;"></div></td><td><code>Beige</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Bisque;"></div></td><td><code>Bisque</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Black;"></div></td><td><code>Black</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:BlanchedAlmond;"></div></td><td><code>BlanchedAlmond</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Blue;"></div></td><td><code>Blue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:BlueViolet;"></div></td><td><code>BlueViolet</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Brown;"></div></td><td><code>Brown</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:BurlyWood;"></div></td><td><code>BurlyWood</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:CadetBlue;"></div></td><td><code>CadetBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Chartreuse;"></div></td><td><code>Chartreuse</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Chocolate;"></div></td><td><code>Chocolate</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Coral;"></div></td><td><code>Coral</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:CornflowerBlue;"></div></td><td><code>CornflowerBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Cornsilk;"></div></td><td><code>Cornsilk</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Crimson;"></div></td><td><code>Crimson</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Cyan;"></div></td><td><code>Cyan</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkBlue;"></div></td><td><code>DarkBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkCyan;"></div></td><td><code>DarkCyan</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkGoldenrod;"></div></td><td><code>DarkGoldenrod</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkGray;"></div></td><td><code>DarkGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkGreen;"></div></td><td><code>DarkGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkKhaki;"></div></td><td><code>DarkKhaki</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkMagenta;"></div></td><td><code>DarkMagenta</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkOliveGreen;"></div></td><td><code>DarkOliveGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkOrange;"></div></td><td><code>DarkOrange</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkOrchid;"></div></td><td><code>DarkOrchid</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkRed;"></div></td><td><code>DarkRed</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkSalmon;"></div></td><td><code>DarkSalmon</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkSeaGreen;"></div></td><td><code>DarkSeaGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkSlateBlue;"></div></td><td><code>DarkSlateBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkSlateGray;"></div></td><td><code>DarkSlateGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkTurquoise;"></div></td><td><code>DarkTurquoise</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DarkViolet;"></div></td><td><code>DarkViolet</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DeepPink;"></div></td><td><code>DeepPink</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DeepSkyBlue;"></div></td><td><code>DeepSkyBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DimGray;"></div></td><td><code>DimGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:DodgerBlue;"></div></td><td><code>DodgerBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Firebrick;"></div></td><td><code>Firebrick</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:FloralWhite;"></div></td><td><code>FloralWhite</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:ForestGreen;"></div></td><td><code>ForestGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Fuchsia;"></div></td><td><code>Fuchsia</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Gainsboro;"></div></td><td><code>Gainsboro</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:GhostWhite;"></div></td><td><code>GhostWhite</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Gold;"></div></td><td><code>Gold</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Goldenrod;"></div></td><td><code>Goldenrod</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Gray;"></div></td><td><code>Gray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Green;"></div></td><td><code>Green</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:GreenYellow;"></div></td><td><code>GreenYellow</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Honeydew;"></div></td><td><code>Honeydew</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:HotPink;"></div></td><td><code>HotPink</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:IndianRed;"></div></td><td><code>IndianRed</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Indigo;"></div></td><td><code>Indigo</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Ivory;"></div></td><td><code>Ivory</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Khaki;"></div></td><td><code>Khaki</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Lavender;"></div></td><td><code>Lavender</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LavenderBlush;"></div></td><td><code>LavenderBlush</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LawnGreen;"></div></td><td><code>LawnGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LemonChiffon;"></div></td><td><code>LemonChiffon</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightBlue;"></div></td><td><code>LightBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightCoral;"></div></td><td><code>LightCoral</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightCyan;"></div></td><td><code>LightCyan</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightGoldenrodYellow;"></div></td><td><code>LightGoldenrodYellow</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightGray;"></div></td><td><code>LightGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightGreen;"></div></td><td><code>LightGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightPink;"></div></td><td><code>LightPink</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightSalmon;"></div></td><td><code>LightSalmon</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightSeaGreen;"></div></td><td><code>LightSeaGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightSkyBlue;"></div></td><td><code>LightSkyBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightSlateGray;"></div></td><td><code>LightSlateGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightSteelBlue;"></div></td><td><code>LightSteelBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LightYellow;"></div></td><td><code>LightYellow</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Lime;"></div></td><td><code>Lime</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:LimeGreen;"></div></td><td><code>LimeGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Linen;"></div></td><td><code>Linen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Magenta;"></div></td><td><code>Magenta</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Maroon;"></div></td><td><code>Maroon</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumAquamarine;"></div></td><td><code>MediumAquamarine</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumBlue;"></div></td><td><code>MediumBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumOrchid;"></div></td><td><code>MediumOrchid</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumPurple;"></div></td><td><code>MediumPurple</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumSeaGreen;"></div></td><td><code>MediumSeaGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumSlateBlue;"></div></td><td><code>MediumSlateBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumSpringGreen;"></div></td><td><code>MediumSpringGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumTurquoise;"></div></td><td><code>MediumTurquoise</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MediumVioletRed;"></div></td><td><code>MediumVioletRed</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MidnightBlue;"></div></td><td><code>MidnightBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MintCream;"></div></td><td><code>MintCream</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:MistyRose;"></div></td><td><code>MistyRose</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Moccasin;"></div></td><td><code>Moccasin</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:NavajoWhite;"></div></td><td><code>NavajoWhite</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Navy;"></div></td><td><code>Navy</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:OldLace;"></div></td><td><code>OldLace</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Olive;"></div></td><td><code>Olive</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:OliveDrab;"></div></td><td><code>OliveDrab</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Orange;"></div></td><td><code>Orange</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:OrangeRed;"></div></td><td><code>OrangeRed</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Orchid;"></div></td><td><code>Orchid</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PaleGoldenrod;"></div></td><td><code>PaleGoldenrod</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PaleGreen;"></div></td><td><code>PaleGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PaleTurquoise;"></div></td><td><code>PaleTurquoise</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PaleVioletRed;"></div></td><td><code>PaleVioletRed</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PapayaWhip;"></div></td><td><code>PapayaWhip</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PeachPuff;"></div></td><td><code>PeachPuff</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Peru;"></div></td><td><code>Peru</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Pink;"></div></td><td><code>Pink</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Plum;"></div></td><td><code>Plum</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:PowderBlue;"></div></td><td><code>PowderBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Purple;"></div></td><td><code>Purple</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Red;"></div></td><td><code>Red</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:RosyBrown;"></div></td><td><code>RosyBrown</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:RoyalBlue;"></div></td><td><code>RoyalBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SaddleBrown;"></div></td><td><code>SaddleBrown</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Salmon;"></div></td><td><code>Salmon</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SandyBrown;"></div></td><td><code>SandyBrown</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SeaGreen;"></div></td><td><code>SeaGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SeaShell;"></div></td><td><code>SeaShell</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Sienna;"></div></td><td><code>Sienna</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Silver;"></div></td><td><code>Silver</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SkyBlue;"></div></td><td><code>SkyBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SlateBlue;"></div></td><td><code>SlateBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SlateGray;"></div></td><td><code>SlateGray</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Snow;"></div></td><td><code>Snow</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SpringGreen;"></div></td><td><code>SpringGreen</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:SteelBlue;"></div></td><td><code>SteelBlue</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Tan;"></div></td><td><code>Tan</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Teal;"></div></td><td><code>Teal</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Thistle;"></div></td><td><code>Thistle</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Tomato;"></div></td><td><code>Tomato</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Turquoise;"></div></td><td><code>Turquoise</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Violet;"></div></td><td><code>Violet</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Wheat;"></div></td><td><code>Wheat</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:White;"></div></td><td><code>White</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:WhiteSmoke;"></div></td><td><code>WhiteSmoke</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:Yellow;"></div></td><td><code>Yellow</code></td></tr>
<tr><td><div style="width:16px;height:16px;margin-right:8px;border:solid 1px #444444;background-color:YellowGreen;"></div></td><td><code>YellowGreen</code></td></tr>
</table>

## **Example**

```text
?text=Once upon a midnight dreary, while I pondered, weak and weary,
Over many a quaint and curious volume of forgotten lore-
While I nodded, nearly napping, suddenly there came a tapping,
As of some one gently rapping, rapping at my chamber door.
	font_family=Courier New
	font_style=bold
```

![Text](text.png)
