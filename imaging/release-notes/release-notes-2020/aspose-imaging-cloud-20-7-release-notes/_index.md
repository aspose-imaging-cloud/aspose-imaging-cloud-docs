---
title: "Aspose.Imaging Cloud 20.7 - Release Notes"
type: docs
url: /aspose-imaging-cloud-20-7-release-notes/
weight: 6
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-580|Check billing process in Imaging for Cloud|
|IMAGINGCLOUD-589|Support saving image files to Dicom format|

In this release, we have added processed file size to billing log and enabled saving to Dicom format.

## **Aspose.Imaging v20.7 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-3960|Incorrect image size after applying Crop/Resize/RotateFlipAll operations on Gif image with subsequent export to WebP|
|IMAGINGNET-3947|Black output after resizing JPG|
|IMAGINGNET-3941|Image saving failed exception when converting EMF|
|IMAGINGNET-3931|Converting to 1 bitdepth PNG results in black background|
|IMAGINGNET-3747|Color information and left margin space is lost on exporting WMF to PDF|
|IMAGINGNET-3925|Exception on rotating big TIFF/PNG/JPEG files|

Aspose.Imaging v20.7 comes with fixing some image conversion and export issues.

For the complete list of changes, please refer to [Aspose.Imaging for .NET 20.7 Release Notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+20.7+-+Release+notes).

## **Usage examples**

**IMAGINGCLOUD-589 Support saving image files to Dicom format**

```
var pathToLocalFile = "ExportSampleImage.bmp";
using (var imageData = File.OpenRead(pathToLocalFile))
{
       string format = "dicom";
       string outPath = null; // Path to updated file (if this is empty, response contains streamed image)
       string storage = null; // Cloud Storage name

       var request = new CreateConvertedImageRequest(inputImageStream, format, outPath, storage);
       Stream updatedImage = this.ImagingApi.CreateConvertedImage(request);
}
```