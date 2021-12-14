---
title: "Use custom fonts"
type: docs
url: /use-custom-fonts/
weight: 120
---

## **Introduction**
Aspose Imaging.Cloud API supported loading custom fonts for vector images.
Custom fonts should be loaded to storage to 'Fonts' folder. 'Fonts' folder should be placed to the root of the cloud storage.

## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

/// <summary>
/// Using custom fonts for vector image conversion example.
/// </summary>
public void UsingCustomFontsForVectorImageConversion()
{	
	string sampleImageFileName = "ImageWithCustomFonts.emz";
	
	// Upload local image to Cloud Storage
	using (var localInputImage = File.OpenRead(Path.Combine(ExampleImagesFolder, sampleImageFileName)))
	{
		var uploadImageRequest = new UploadFileRequest(Path.Combine(CloudPath, imageName), image);
		ImagingApi.UploadFile(uploadImageRequest);
	}

	// custom fonts should be loaded to storage to 'Fonts' folder
	// 'Fonts' folder should be placed to the root of the cloud storage
	using (var font = File.OpenRead( Path.Combine(ExampleImagesFolder, "Fonts", "Gibson-Regular.ttf")))
	{
		var uploadFontRequest = new UploadFileRequest(Path.Combine("Fonts", "Gibson-Regular.ttf"), font);
		ImagingApi.UploadFile(uploadFontRequest);
	}

	var folder = CloudPath; // Input file is saved at the Examples folder in the storage
	string storage = null; // Cloud Storage name
	var request = new ConvertImageRequest(sampleImageFileName, "png", folder, storage);


	using (var updatedImage = ImagingApi.ConvertImage(request))
	{	
		// Save updated image to local storage
		using (var fileStream = File.Create(Path.Combine(ExampleImagesFolder, "GrayscaleSampleImage_out.png")))
		{
			updatedImage.Seek(0, SeekOrigin.Begin);
			updatedImage.CopyTo(fileStream);
		}
	}
}

{{< /tab >}}

{{< tab tabNum="2" >}}

/**
* Using custom fonts for vector image conversion example.
* @throws Exception 
*/
public void usingCustomFontsForVectorImageConversion() throws Exception
{
	String imageFileName = "ImageWithCustomFonts.emz";
	
	byte[] inputImage = Files.readAllBytes(Paths.get(ExampleImagesFolder, imageFileName));
	UploadFileRequest imageRequest = new UploadFileRequest(Paths.get(CloudPath, imageFileName).toString(), inputImage, null);
    ImagingApi.uploadFile(imageRequest);

	// custom fonts should be loaded to storage to 'Fonts' folder
	// 'Fonts' folder should be placed to the root of the cloud storage
	byte[] font = Files.readAllBytes(Paths.get(ExampleImagesFolder, "Fonts", "Gibson-Regular.ttf"));
	UploadFileRequest fontRequest = new UploadFileRequest(Paths.get("Fonts", "Gibson-Regular.ttf").toString(), font, null);
    ImagingApi.uploadFile(fontRequest);

	String format = "png";
	String folder = CloudPath; // Input file is saved at the Examples folder in the storage
	String storage = null; // Cloud Storage name
	ConvertImageRequest request = new ConvertImageRequest(imageFileName, format, folder, storage);	
	byte[] updatedImage = ImagingApi.convertImage(request);	
	
	Path path = Paths.get(OutputFolder, "ImageWithCustomFonts_out.png").toAbsolutePath();
    Files.write(path, updatedImage);	
}

{{< /tab >}}

{{< /tabs >}}