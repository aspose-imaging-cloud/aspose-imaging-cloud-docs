---
title: "Aspose.Imaging Cloud 20.4 - Release Notes"
type: docs
url: /aspose-imaging-cloud-20-4-release-notes/
weight: 9
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-496|CDR to PDF conversion misses the text|
|IMAGINGAINET-238|Add stream response feature and tests for tiff to fax requests|
|IMAGINGAINET-278|Add support for Frames API for all applicable formats|

In this release we have supported Frames API for all applicable formats, added tiff to fax API method, fixed the issue with CDR to PDF conversion, and supported of  Aspose.PSD as backend dll for Psd images.

***Please note*: starting from version 20.4 we don`t support conversion from PSD to WEBP.**

## **Aspose.Imaging v20.4 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-3788|Implement support text in the CDR format on X3 and below versions|
|IMAGINGNET-3679|Remove PSD loading support from Aspose.Imaging|
|IMAGINGNET-3795|Aspose.Imaging 20.2: Conversion of particular WMF to PNG throws exception|
|IMAGINGNET-3770|Cannot access a disposed object; Object name: 'DjvuImage'|
|IMAGINGNET-3774|Converting EMF to PNG adds a border around PNG|

Aspose.Imaging v20.4 comes with fixing some image conversion issues and removed PSD loading and conversion.

For the complete list of changes, please refer to [Aspose.Imaging for .NET 20.4 Release Notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+20.4+-+Release+notes).

## **API changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-238|Add stream response feature and tests for tiff to fax requests|
|IMAGINGCLOUD-278|Add support for Frames API for all applicable formats|

## **Aspose.Imaging Cloud SDK changes**
|     |     |
| --- | --- |
|IMAGINGAINET-238|Add stream response feature and tests for tiff to fax requests|
|IMAGINGAINET-278|Add support for Frames API for all applicable formats|

- supported Frames API for all applicable formats,
- added tiff to fax API method

## **Usage examples**

**IMAGINGNET-238 Add stream response feature and tests for tiff to fax requests**
```
var pathToLocalFile = "test.tiff";
using (var imageData = File.OpenRead(pathToLocalFile))
{
  var request = new CreateFaxTiffRequest(imageData);
  var faxTiff = ImagingApi.CreateFaxTiff(request);
}
```
**IMAGINGNET-278 Add support for Frames API for all applicable formats**
```
// GetFrame range
var cloudFileName = "MultipageFile.djvu";
var startFrameId = 17;
var endFrameId = 23;
var request = new GetImageFrameRangeRequest(cloudFileName, startFrameId, endFrameId);
var frameRange = ImagingApi.GetImageFrameRange(request);
// save result to local file
using (var fileStream = File.Create(framePath))
{
    frameRange.Seek(0, SeekOrigin.Begin);
    frameRange.CopyTo(fileStream);
}

// Create Frame range:
var pathToLocalFile = "MultipageFile.djvu";
using (var imageData = File.OpenRead(pathToLocalFile))
{
  var startFrameId = 17;
  var endFrameId = 23;
  var request = new CreateImageFrameRangeRequest(imageData, startFrameId, endFrameId);
  var frameRange = ImagingApi.CreateImageFrameRange(request);

 // save result to local file
 using (var fileStream = File.Create(framePath))
 {
      frameRange.Seek(0, SeekOrigin.Begin);
      frameRange.CopyTo(fileStream);
 }
}
```