---
title: Contract for Financial services (.txt)
type: docs
weight: 5
url: /net/showcases/bank/txt
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
?page=1
?container=header
	columns_proportions=60%-40%
?block=left
	column=1
?content=The West Federal Bank
	font_size=14
	font_style=bold
	font_family=Cambria
&block
?block=right
	column=2
?content=Application form
	font_size=14
?barcode=form id
	value=ESK3JFSGHEJFSDA
	codetext=true
	barcode_type=QR
	x=2000
	width=200
	height=200
&block
&container
?container=personal
	columns_count=2
?block=left
	column=1
?content=Personal information
	font_size=12
	font_style=bold
	font_family=Cambria
&block
&container
?container=information
	columns_count=2
?block=left
	column=1
?content=Name: John Michael Davis
?content=Date of birth: 5/10/1982
?content=Passport: E009F62768
&block
?block=right
	column=2
?content=Mobile phone:+1 456-782-9834
?content=E-mail: d.davis@gmail.com
&block
&container
?text=Terms and Conditions
	font_style=bold
	font_size=12
	font_family=Cambria
?container=terms
	columns_count=2
?block=left
	column=1
?content=We have a range of products designed to suit your personal banking needs, some of which maybe accessed through our electronic banking services. The specific features of our products are available on request. Some products may not be available to you depending on your location. Depending on your location, some products may not be accessible through our electronic banking services. Your electronic access to such products may be withdrawn, amended,terminated or suspended at any time without notice, to the extent permitted by applicable law sand regulations. 
?content=1.2 If you want to access or use a product in any manner including electronically, you need to complete an application to ask us to approve your use of it. Different eligibility criteria may apply to different products. These may include minimum or maximum age or deposit amounts.Fees, commissions or other charges may apply for such access or use. We may refuse an application for any reason. Unless required by law, we do not need to give you a reason.
?content=1.3 Our electronic banking services are available to you only after we have approved it for your use.
&block
?block=right
	column=2
?content=1.4 If we agree to provide a product to you and allow you to access or use a product through our electronic banking services, the terms on which you may use the product are called our “banking agreement”. This is made up of the following documents for the product:the application; any letter of offer ; these Client terms; the product terms; our approval; the tariff sheet; any guidelines we issue in connection with use of the product (including guidelines for use of electronic banking services); any other terms and conditions that form part of our banking agreement as varied or replaced from time to time. A separate banking agreement is entered into each time you and we agree that you may use a product. For example, if you accept a letter of offer for more than one product, a separate “banking agreement” is established at that time for each product on the terms set out, or referred to, in the letter of offer. The terms of our banking agreement apply to each access or use of the product including any access or use of the product through our electronic banking services, by you or any authorized person. If you or an authorized person does not agree with the terms of our banking agreement, you or they should not carry out the transaction or access any account. You are responsible for ensuring that each authorized person complies with our banking agreement and for anything an authorized person does in connection with our banking agreement. You must ensure that each authorized person is given a copy of the terms that apply to any product they use and this Client terms. 
?content=1.5 If you are not a resident of City, additional terms and conditions may apply as notified by us at any time.
&block
&container
?text=______________________________________________________________________________________________________________
?text=Service details
	font_style=bold
	font_size=12
	font_family=Cambria
?container=service
	columns_count=1
?block=access
	column=1
?content=Access information:
	font_style=italic
?content=Your temporary password would be send to mobile phone stated in field "Mobile phone"(required) of section "Personal Information" of current application.
&block
&container
?text=Account information:
	font_style=italic
?container=accounts
	columns_count=2
?block=
	column=1
?content=Master account - No. 4654897239 - USD
?content=Master account - No. 4658585887 - EUR
&block
&container
?container=checkboxes
	columns_count=1
?block=left
	column=1
?checkbox=email
	hide_name=true
?content=I don't want to receive e-mail notifications
	align=right
&checkbox
?empty_line=10
&block
?block=left
	column=1
?checkbox=sms
	hide_name=true
?content=I don't want to receive sms notifications
	align=right
&checkbox
&block
&container
?empty_line=
	height=40
?container=
	columns_proportions=50%-50%
?block=1
	column=1
	is_clipped=true
?content=_______________________________________
	align=right
?content=X Apllicant's Signature
	align=right
&block
?block=2
	column=2
	is_clipped=true
?content=_________________
	align=right
?content=Date
	align=right
&block
&container
&page
```

</details>

**Template result**

**![todo:image_alt_text](bank-txt.png)**