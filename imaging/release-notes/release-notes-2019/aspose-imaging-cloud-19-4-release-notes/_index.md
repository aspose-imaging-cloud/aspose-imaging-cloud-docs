---
title: "Aspose.Imaging Cloud 19.4 - Release Notes"
type: docs
url: /aspose-imaging-cloud-19-4-release-notes/
weight: 10
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-285|Check and fix DB records about methods on production|
|IMAGINGCLOUD-287|Enable CDR tests|
|IMAGINGCLOUD-291|Enable CompareImagesTests|
|IMAGINGCLOUD-159|Make product a microservice|
|IMAGINGCLOUD-290|Integrate Aspose.Imaging v19.4 assembly|
|IMAGINGCLOUD-271|Review and enable universal Aspose.Imaging Cloud API entries across all image formats|

We have taken time since version 19.1 to migrate to new architecture and enrich Aspose.Imaging 19.4 with improved performance and enhanced formats support!

In this release:

- We have added support of CDR, CMX, DJVU and PDF formats, along with enhanced cross-format conversion for common operations. Please, look at the [common operations format support map](/supported-file-formats/#supportedfileformats-commonoperationsformatsupportmap) to see what you can achieve!
- Image rendering quality for export, resize and rotate/flip operations became better
- Resize operation performance for CDR, CMX, SVG, EMF and WMF vector formats has been improved
- AI features subsystem has been reworked to improve both performance and stability
- Advanced EMF and WMF processing APIs now allow to save the result in different formats
- Several problematic APIs have been fixed
- Storage APIs from now on are included in Imaging for better user experience and unification

## **Aspose.Imaging v19.4 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-3258|Add Device Independent Bitmap File (.dib) file format support|
|IMAGINGNET-3305|Incorrect conversion of specific WMF images to SVG and PNG|
|IMAGINGNET-3203|PSD performance fell down several times|
|IMAGINGNET-3251|Saving EMF as SVG the resulting transformation is incorrect|
|IMAGINGNET-3338|Preserve transparency converting tif image to transparent png with resize|

Now, you can use DIB format specification parameter (which is technically BMP), enjoy several times faster PSD processing and improved conversion features!

For the complete list of changes, please refer to [Aspose.Imaging for .NET 19.4 Release Notes ](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+19.4+-+Release+Notes).

## **API changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-233|Refactor SaaSposeResponse|
|IMAGINGCLOUD-232|Release the API v3|

Aspose.Imaging 19.4 comes with more robust APIs and **breaking changes**:

- PNG, DNG, ODG and DICOM APIs has been removed since they were supporting only simple conversion without any advanced processing parameters - please, use *Save As* APIs for export operations regarding these formats from now on. It's possible that some of the removed APIs will be added later in the future if applicable features are implemented
- Legacy SaaSposeResponse response format has been removed

Please, refer to updated [API reference page](https://apireference.aspose.cloud/imaging/).

## **Aspose.Imaging Cloud SDK Changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-270|.NET SDK SaveAs POST request exception|
|IMAGINGCLOUD-272|Fix .NET SDK Newtonsoft.Json version reference for NuGet|
|IMAGINGCLOUD-288|Update SDKs for API v3|
|IMAGINGCLOUD-273|Explore links to Storage resources in SDK examples for users|
|IMAGINGCLOUD-295|Add .NET Standard support to .NET SDK|

.NET SDK references has been fixed and now it also supports .NET Standard 2.0.

API error handling has been improved to include enhanced information.

Regarding Storage APIs, since version 19.4 all SDKs include support of storage operations for better user experience and unification, so now there is no need to use two different SDKs!

It gives you an ability to:

- Upload, download, copy, move and delete files, including versions handling (if you are using Cloud storage that supports this feature - true by default)
- Create, copy, move and delete folders
- Copy and move files and folders accross separate storages in scope of a single operation
- Check if certain file, folder or storage exists

Please, check the updated ***Examples.md*** file in the root of the SDK [repository](https://github.com/aspose-imaging-cloud) you need to look for common Storage operations usage examples and enhanced error handling.

The main **breaking change** is removal of PNG, DNG, ODG and DICOM processing methods along with legacy response format (which affects the minority of operations) according to web APIs update.

***Note:*** in one of the next releases, we plan to seriously improve SDKs usability by refactoring method names, which will also be a breaking change.
