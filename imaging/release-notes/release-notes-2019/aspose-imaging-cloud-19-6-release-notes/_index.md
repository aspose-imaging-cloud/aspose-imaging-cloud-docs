---
title: "Aspose.Imaging Cloud 19.6 - Release Notes"
type: docs
url: /aspose-imaging-cloud-19-6-release-notes/
weight: 60
---

## **New features, fixes and improvements**
|     |     |
| --- | --- |
|IMAGINGCLOUD-266|Enable parallel DJVU tests|
|IMAGINGCLOUD-267|Remove caching before crop for WebP format|
|IMAGINGCLOUD-281|Fix DJVU multi-page export to PSD|
|IMAGINGCLOUD-283|Enable WebP self-update test|
|IMAGINGCLOUD-286|Enable parallel EMF tests|
|IMAGINGCLOUD-297|ExtractAndAddImageFeaturesFromFolderTest fix|
|IMAGINGCLOUD-282|Enable WMF and EMF crop operations|
|IMAGINGCLOUD-342|Improve Cloud solution module structure|

In this release we have:

- Continuously worked on AI subsystem improvements, and now it is much more stable than ever before!
- Fixed advanced WebP processing
- Fixed and improved DJVU format processing which improved multi-page export quality
- Fixed and improved EMF and WMF crop operations
- Enriched our common ops functionality which is reflected in the [common operations format support map](/supported-file-formats/#supportedfileformats-commonoperationsformatsupportmap) for you to be able to save the processing results to even more formats!

## **Aspose.Imaging v19.6 release integration features**
|     |     |
| --- | --- |
|IMAGINGNET-3376|Backport Aspose.Psd code to Aspose.Imaging April/2019|
|IMAGINGNET-3321|Large memory consumption while loading a PNG image|
|IMAGINGNET-3287|Margins are getting added when converting WMF to SVG|
|IMAGINGNET-3378|Image width and height is cropped on converting WMF to PNG|
|IMAGINGNET-3421|Gif file not properly converted to PDF|
|IMAGINGNET-3205|RotateFlip operation does not work as expected with PSD|
|IMAGINGNET-3374|Issue with converting DjVu format to images|
|IMAGINGNET-3309|Wmf to PNG not properly converted|
|IMAGINGNET-3279|EMF and WMF crop operations provide invalid results|
|IMAGINGNET-3395|EMF not properly converted to SVG|
|IMAGINGNET-3266|Fix parallel DJVU processing and check for memory leaks|
|IMAGINGNET-3265|Fix WebP crop operation - it requires caching for some reason|
|IMAGINGNET-3282|Fix enormous WebP animation RAM consumption in case of self-update|

Aspose.Imaging Cloud v19.6 comes with various formats improvements' integration to be able to cover even wider range of specific features and use-cases!

For the complete list of changes, please refer to [Aspose.Imaging for .NET 19.6 Release Notes](https://docs.aspose.com/display/imagingnet/Release+Notes+-+2019).

## **API changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-350|Make error responses camel case|
|IMAGINGCLOUD-341|Deprecate support of creating a resource with GET requests|
|IMAGINGCLOUD-351|Update Storage submodule.|

In this release, we are introducing some major changes which have been announced in the previous release. They are based on industries' best practices regarding REST APIs implementation:

- We have updated our Storage submodule, and now the Storage API uses ***PUT*** (instead of ***POST***) for idempotent operations of file uploading and folders creation.
- We have deprecated GET requests that were able to create resources. Practically, it does mean that from now on you can only obtain the processed image in the response stream with GET requests, and saving it to storage (i.e. creating a new resource) is no longer allowed (***outPath*** parameter has been removed for these requests). If you still need to process the image from storage and save it to storage as well, please upload the processed image explicitly by using the Storage API.

Please, refer to the updated [API reference page](https://apireference.aspose.cloud/imaging/).

For more information on how it is reflected in SDKs, please read the information in the SDK section below.

***Note:*** with the new API v4.0 which is planned to be released this year, we will continue making our APIs more RESTful and robust.

## **Aspose.Imaging Cloud SDK Changes**
|     |     |
| --- | --- |
|IMAGINGCLOUD-324|Fix Android gradle script that uses repo dependency for tests|
|IMAGINGCLOUD-330|Aspose.Imaging Cloud Java SDK vulnerability|
|IMAGINGCLOUD-307|Add common operations format support map link to SDK readme files|
|IMAGINGCLOUD-298|Add missing values documentation for string parameters|
|IMAGINGCLOUD-294|Improve API reference groups and SDK methods naming to make them more user- and SEO-friendly|

The small fixes are the usage of more recent libraries in Java SDK to eliminate the possible security vulnerability, improving SDK documentation and adding the [common operations format support map](/supported-file-formats/#supportedfileformats-commonoperationsformatsupportmap) to SDK READMEs.

The main change that has been announced in the previous release is the ***method naming scheme change***. In conjunction with making API more RESTful, we have greatly improved the usability of our SDKs.

The common logic was to make SDK methods naming simple and intuitive instead of previous bulky approach. For the most of updates, it's true that GET requests contain simple operation name and POST requests which allow us to create resources start with *Create*, the ones that don't - with *Extract*.

|**Old method name**|**New method name**|
| :- | :- |
|GetImageResize|ResizeImage|
|PostImageResize|CreateResizedImage|
|GetImageCrop|CropImage|
|PostImageCrop|CreateCroppedImage|
|GetImageRotateFlip|RotateFlipImage|
|PostImageRotateFlip|CreateRotateFlippedImage|
|GetImageSaveAs|SaveImageAs|
|PostImageSaveAs|CreateSavedImageAs|
|GetImageUpdate|UpdateImage|
|PostImageUpdate|CreateUpdatedImage|
| | |
|GetImageProperties|GetImageProperties|
|PostImageProperties|ExtractImageProperties|
| | |
|GetImageFrame|GetImageFrame|
|GetImageFrameProperties|GetImageFrameProperties|
|PostImageFrame|CreateImageFrame|
|PostImageFrameProperties|ExtractImageFrameProperties|
| | |
|GetImageBmp|ModifyBmp|
|PostImageBmp|CreateModifiedBmp|
|GetImageGif|ModifyGif|
|PostImageGif|CreateModifiedGif|
|GetImageJpg|ModifyJpeg|
|PostImageJpg|CreateModifiedJpeg|
|GetImagePsd|ModifyPsd|
|PostImagePsd|CreateModifiedPsd|
|GetImageWebP|ModifyWebP|
|PostImageWebP|CreateModifiedWebP|
|GetImageJpeg2000|ModifyJpeg2000|
|PostImageJpeg2000|CreateModifiedJpeg2000|
|GetImageEmf|ModifyEmf|
|PostImageEmf|CreateModifiedEmf|
|GetImageWmf|ModifyWmf|
|PostImageWmf|CreateModifiedWmf|
|GetImageTiff|ModifyTiff|
|PostImageTiff|CreateModifiedTiff|
| | |
|GetTiffToFax|ConvertTiffToFax|
|PostTiffAppend|AppendTiff|
| | |
|PostCreateSearchContext|CreateImageSearch|
|GetSearchContextStatus|GetImageSearchStatus|
|DeleteSearchContext|DeleteImageSearch|
|GetSearchContextFindSimilar|FindSimilarImages|
|GetSearchContextFindDuplicates|FindImageDuplicates|
|PostSearchContextAddTag|CreateImageTag|
|GetSearchContextExtractImageFeatures|ExtractImageFeatures|
|PostSearchContextExtractImageFeatures|CreateImageFeatures|
|GetSearchContextImageFeatures|GetImageFeatures|
|DeleteSearchContextImageFeatures|DeleteImageFeatures|
|PutSearchContextImageFeatures|UpdateImageFeatures|
|PostSearchContextAddImage|AddSearchImage|
|GetSearchContextImage|GetSearchImage|
|DeleteSearchContextImage|DeleteSearchImage|
|PutSearchContextImage|UpdateSearchImage|
|PostSearchContextCompareImages|CompareImages|
|PostSearchContextFindByTags|FindImagesByTags|

Please, check the updated *Examples.md* file in the root of the needed SDK [repository](https://github.com/aspose-imaging-cloud): it contains new names and also covers the case when GET request result is uploaded to the storage explicitly.

***Note:*** the new API v4.0 which is planned to be released this year should not affect SDK methods naming much since the scheme introduced in the current release is designed to be mostly compatible with this change.
