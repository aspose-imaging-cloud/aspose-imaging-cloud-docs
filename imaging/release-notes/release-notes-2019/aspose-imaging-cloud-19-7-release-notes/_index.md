---
title: "Aspose.Imaging Cloud 19.7 - Release Notes"
type: docs
url: /aspose-imaging-cloud-19-7-release-notes/
weight: 6
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-360|Storage API upload bug workaround|
|IMAGINGCLOUD-374|Storage API move and copy operation bugs workaround|

In this release we have fixed Storage API upload/copy/move file bug when corresponding requests return positive result, though check for existence returns negative one.

## **Aspose.Imaging v19.7 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-2926|Saving PSD into PDF does not provide selectable text|
|IMAGINGNET-3381|Support optimization strategy in PartialRotater class|
|IMAGINGNET-2044|Support for OTG (OpenDocument graphics template)|
|IMAGINGNET-3450|EMF to PNG conversion gives the wrong position of the text labels|
|IMAGINGNET-3442|Bpmn.io SVG converting results in strange PNGs|
|IMAGINGNET-3230|Converting Jpeg to Tiff results in improper green overlay|
|IMAGINGNET-3444|Aspose.Imaging issue with resize SVG image|

Aspose.Imaging Cloud v19.7 comes with various formats improvements' integration to be able to cover even wider range of specific features and use-cases, including **OTG format support** (please, check our updated [format support page](/supported-file-formats/)) and continuous work on memory efficiency improvements which resulted in increased service resilience.

For the complete list of changes, please refer to [Aspose.Imaging for .NET 19.7 Release Notes](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+19.7+-+Release+Notes).

## **API changes**

None.

## **Aspose.Imaging Cloud SDK Changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-366|Increase SDK clients timeout|
|IMAGINGCLOUD-216|Integrate Imaging for Cloud Python SDK auto-generation|
|IMAGINGCLOUD-289|Integrate externally added SDK examples|
|IMAGINGCLOUD-359|Change SDK info urls from <https://products.aspose.cloud/imaging/cloud> to <https://products.aspose.cloud/imaging>|
|IMAGINGCLOUD-363|Update SDKs to use OnPremise name instead of IsMetered and state that this feature is experimental|

- Continued our work on extension of Aspose.Imaging Cloud ecosystem, which resulted in **the all-new Python SDK**!
- Added sophisticated examples for [.NET](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-dotnet) and [Java](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) SDKs (please, check the *Examples* folder).
- Increased request timeout for SDKs.
- Prepared our SDKs for future Docker Hub release of a Docker image for on-premise deployment which will use metered licensing model.


