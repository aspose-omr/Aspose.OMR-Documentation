---
weight: 10
date: "2023-06-08"
author: "Vladimir Lapin"
type: docs
url: /cpp/omr-technology/
feedback: OMRCPP
title: Optical mark recognition (OMR) overview
description: What is Optical Mark Recognition (OMR), where is it used, and how is the technology evolving.
keywords:
- OMR
- form
- recognition
- technology
- concept
---

Even if you have never heard of **Optical Mark Recognition (OMR)** technology before, you have probably come across it more than once in your life. It is used everywhere to automatically recognize a large number of hand-filled uniform sheets in which you answer a question by drawing a random mark, hence the technology's name, in a circle or box (generally referred as "bubble"). Exams, elections, hand-filled surveys, border entry forms, customs declarations, health insurance applications, and similar documents are just a narrow set of use cases.

Manually reading and aggregating results from hundreds and thousands of manually completed forms is a long and laborious process with a high potential for human error. OMR fully automates the process, allowing hundreds of sheets per minute to be recognized with almost 100% accuracy. Results can be directly imported into a database or spreadsheet for further aggregation and analysis. OMR processing is often accompanied by [optical character recognition (OCR)](https://products.aspose.app/ocr) to read the contents of handwritten fields.

![Optical mark recognition process](omr-technology.png)

The recognition process can involve quite sophisticated technologies, but it usually involves checking whether the light is passing through the paper or reflecting. Filled/marked areas will reflect less light than blank paper, resulting in a less reflection. The result is then checked against a predefined pattern and digitized.

Historically, OMR required the use of specialized scanners (optical mark readers), special paper, magnetic ink, and other "hardware" solutions. Providing unsurpassed recognition speed and accuracy, this equipment is very expensive and not available in a regular store. This makes these devices and supplies unsuitable for SMBs, organizations, schools, casual or occasional jobs.

This is where modern technology comes to the rescue. Computer vision and machine-learning techniques have made it possible to use an ordinary pen and paper, regular office equipment or even a smartphone camera instead of specialized devices. Recognition accuracy and reliability are comparable to the industry-grade hardware solutions. This allows you to create pure **software OMR solutions** that compete with traditional hardware systems at a much lower cost.

Aspose has made one step further by offering a universal **OMR API** as a C++ programming library - **Aspose.OMR for C++**. With it, you can build an OMR application that [ideally](/omr/cpp/features-benefits/) matches your requirements in literally less than 10 lines of code.
