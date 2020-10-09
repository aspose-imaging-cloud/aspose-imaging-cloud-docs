---
title: "Aspose.Imaging Cloud 18.11 - Release Notes"
type: docs
url: /aspose-imaging-cloud-18-11-release-notes/
weight: 110
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-185|Integrate Aspose.Imaging v18.11|
|IMAGINGCLOUD-180|Integrate with status.aspose.cloud|
|IMAGINGCLOUD-196|Add possibility to read image properties and manipulate image frames from stream|

For the complete list of changes, please refer to [Aspose.Imaging for .NET 18.11 Release Notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+18.11+-+Release+Notes).

## **API Changes**

Starting from this version, it is possible to get image properties, TIFF frame properties, and manipulate TIFF frames using HTTP streams! Before, the only option was to use images from storage with GET requests, and now we provide POST alternatives for your convenience.

Please, look at the updated [API reference page](https://apireference.aspose.cloud/imaging/).

## **Aspose.Imaging Cloud SDK changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-193|Potential security vulnerability in Aspose.Imaging for Cloud SDK dependencies|
|IMAGINGCLOUD-194|Check and fix OAuth in SDKs|
|IMAGINGCLOUD-78|Add support for Android to Java SDK|
|IMAGINGCLOUD-203|Improve response types handling in Java SDK|

Along with this release, we have introduced the Aspose.Imaging Cloud **Android SDK** (to be more precise, Java SDK modifications and instructions for Android support), which you can get from [GitHub repository](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-android).

SDKs were updated to include Aspose.Imaging API changes.

Examples were updated to demonstrate the error codes handling.

Installation instructions have been added.

The breaking change of Java SDK is types handling, which is described in updated [GitHub](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) examples. Before, users should process basic response class which contained needed response object inside, and cast this object to the needed type. Now, our APIs return typed response objects at once for your convenience.


