---
title: "Aspose.Imaging Cloud 20.6 - Release Notes"
type: docs
url: /aspose-imaging-cloud-20-6-release-notes/
weight: 60
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-559|Rename saveAs API method to convert|
|IMAGINGCLOUD-572|Add "allowlabels" and "blocklabels" parameters to object detection api requests|
|IMAGINGCLOUD-560|Visual object detection duplicates borders|

In this release, we have extended parameters in the object detection API and renamed SaveAs API method to Convert.

## **API changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-559|Rename saveAs API method to convert|
|IMAGINGCLOUD-572|Add "allowlabels" and "blocklabels" parameters to object detection api requests|

## **Aspose.Imaging Cloud SDK changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-559|Rename saveAs API method to convert|
|IMAGINGCLOUD-574|Add allowedLabels and blockedLabels object detection parameters to SDK|

- fixed vulnerabilities for Java SDK
- supported new parameters for the object detection in the all SDKs
- renamed SaveAs methods to Convert

## **Usage examples**

**IMAGINGCLOUD-559 Rename saveAs API method to convert**

```
var pathToLocalFile = "ExportSampleImage.bmp";
using (var imageData = File.OpenRead(pathToLocalFile))
{
       string format = "pdf";
       string outPath = null; // Path to updated file (if this is empty, response contains streamed image)
       string storage = null; // Cloud Storage name

       var request = new CreateConvertedImageRequest(inputImageStream, format, outPath, storage);
       Stream updatedImage = this.ImagingApi.CreateConvertedImage(request);
}
```

**IMAGINGCLOUD-574 Add "allowlabels" and "blocklabels" parameters to object detection api requests**

```
var SampleImageFileName = "object_detection_example.jpg";
using (FileStream inputImageStream = File.OpenRead(Path.Combine(ExampleImagesFolder, SampleImageFileName)))
{
    var method = "ssd";
    var threshold = 50;
    var includeClass = true;
    var includeScore = true;
    var allowedLabels = "cat,person";
    var blockedLabels = "dog";
    string outPath = null;
    string storage = null; 

    var request = new CreateObjectBoundsRequest(inputImageStream, method, threshold, includeClass, includeScore, allowedLabels, blockedLabels, outPath, storage);

    DetectedObjectList detectedObjectList = this.ImagingApi.CreateObjectBounds(request);                
}
```