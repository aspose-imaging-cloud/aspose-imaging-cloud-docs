---
title: "Aspose.Imaging Cloud 20.8 - Release Notes"
type: docs
url: /aspose-imaging-cloud-20-8-release-notes/
weight: 5
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|MAGINGCLOUD-578|Support additional image formats in Object Detection|
|IMAGINGCLOUD-605|Support load images in EPS format|

In this release, we have supported additional image formats in object detection and loading images in EPS format.

## **Aspose.Imaging v20.8 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-3732|Enhance EPS format support|
|IMAGINGNET-2243|Support to load and convert EPS file PDF/A format|
|IMAGINGNET-4033|Black output after resizing PNG and saving to JPG|
|IMAGINGNET-3977|Exception on loading webp image|
|IMAGINGNET-3974|Object reference not set to an instance of an object exception when saving JP2|
|IMAGINGNET-3973|Undefined function "if" exception when saving ODG|
|IMAGINGNET-3748|WMF image is cut on right in exported PDF|
|IMAGINGNET-2981|Exception on converting EPS|

Aspose.Imaging v20.8 comes with improving support of ESP format, fixing image loading and saving issues for some formats.

For the complete list of changes, please refer to [Aspose.Imaging for .NET 20.8 Release Notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+20.8+-+Release+notes).

## **Aspose.Imaging Cloud SDK changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-605|Support load images in EPS format|

- supported EPS format in all the SDKs

## **Usage examples**

**IMAGINGCLOUD-605 Support load images in EPS format**

```
var pathToLocalFile = "ExportSampleImage.eps";
using (var imageData = File.OpenRead(pathToLocalFile))
{
        string format = "png";
        string outPath = null; // Path to updated file (if this is empty, response contains streamed image)
        string storage = null; // Cloud Storage name

        var request = new CreateConvertedImageRequest(inputImageStream, format, outPath, storage);
        Stream updatedImage = this.ImagingApi.CreateConvertedImage(request);
}
```