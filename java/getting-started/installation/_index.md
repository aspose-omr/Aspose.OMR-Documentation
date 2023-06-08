---
weight: 20
date: "2023-06-06"
author: "Vladimir Lapin"
type: docs
url: /java/installation/
feedback: OMRJAVA
title: Installation
description: Installing Aspose.OMR for Java from the Maven repository.
keywords:
- install
- update
- Maven
- package
---

**Aspose.OMR for Java** is hosted in the [Maven repository](https://releases.aspose.com/java/repo/com/aspose/aspose-omr/). You can easily use it directly in your Maven Projects with minimal configuration. There is no need to download and install any additional software - the package is self-contained.

## Configuring the repository

Specify Aspose Maven Repository location by adding the following lines to your Maven **pom.xml** configuration file:

```xml
<repositories>
	<repository>
		<id>AsposeJavaAPI</id>
		<name>Aspose Java API</name>
		<url>https://releases.aspose.com/java/repo/</url>
	</repository>
</repositories>
```

## Dependencies

Specify the minimal required dependencies for Aspose.OMR for Java package. Add the following lines to your Maven **pom.xml** configuration file:

```xml
<dependency>
	<groupId>com.aspose</groupId>
	<artifactId>aspose-omr</artifactId>
	<version>23.5</version>
	<classifier>jdk6</classifier>
</dependency>
<dependency>
	<groupId>com.aspose</groupId>
	<artifactId>aspose-omr</artifactId>
	<version>23.5</version>
	<classifier>javadoc</classifier>
</dependency>
```

{{% alert color="primary" %}} 
Do not forget to change the version number to the current version of the Aspose.OMR for Java package. View the [Release Notes](/omr/java/release-notes/) for the latest changes, improvements, bug fixes, and backward compatibility information.
{{% /alert %}} 
