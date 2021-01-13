---
title: "Aspose.Imaging Cloud 20.5 - Release Notes"
type: docs
url: /aspose-imaging-cloud-20-5-release-notes/
weight: 8
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-515|Extend SaveAs functionality|
|IMAGINGCLOUD-494|Add object detection and classification feature|
|IMAGINGCLOUD-531|Fix vulnerabilities for Aspose.Imaging Cloud Java SDK|

In this release we have extended export to Dicom and Html5 canvas, added object detection and classification feature, and fixed vulnerabilities in the Java SDK.

## **API changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-494|Add object detection and classification feature|

## **Aspose.Imaging Cloud SDK changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-531|Fix vulnerabilities for Aspose.Imaging Cloud Java SDK|
|IMAGINGCLOUD-494|Add object detection and classification feature|

- fixed vulnerabilities and updated java jdk version to 1.8.0_251 for Java SDK
- supported object detection and classification feature in the all SDKs

## **Usage examples**

**IMAGINGCLOUD-515 Extend SaveAs functionality**

```
var pathToLocalFile = "ExportSampleImage.bmp";
using (var imageData = File.OpenRead(pathToLocalFile))
{
  var format ="html5";
  var folder = null; 
  string storage = null; 
  var request = new CreateSavedImageAsRequest(inputImageStream, format, folder, storage);
  var updatedImage = ImagingApi.CreateSavedImageAs(request);
}
```

**IMAGINGCLOUD-494 Add object detection and classification feature**

```
var SampleImageFileName = "object_detection_example.jpg";
using (FileStream inputImageStream = File.OpenRead(Path.Combine(ExampleImagesFolder, SampleImageFileName)))
{
    var method = "ssd";
    var threshold = 50;
    var includeClass = true;
    var includeScore = true;
    string outPath = null;
    string storage = null; 

    var request = new CreateObjectBoundsRequest(inputImageStream, method, threshold, includeClass, includeScore, outPath, storage);

    DetectedObjectList detectedObjectList = this.ImagingApi.CreateObjectBounds(request);                
}
```