---
title: "Get Image Features from Search Context"
type: docs
url: /get-image-features-from-search-context/
weight: 110
---

## **Introduction**

This article explains how to get image features from search context.

The API URL is: [GET /imaging/ai/imageSearch/{searchContextId}/features](https://apireference.aspose.cloud/imaging/#/SearchContextFeatures/GetImageFeatures)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContextFeatures/GetImageFeatures) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and there parameters are also given there.

## **cURL Example**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get Access Token
// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/oauth2/token" \
-X POST \
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"



// cURL example to get image features from search context

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/cc435948-2dc3-4269-9299-052baa314d72/features?imageId=WaterMark.bmp" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <access_token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Message": "Features for image with WaterMark.bmp not found"

}

```

{{< /tab >}}

{{< /tabs >}}

## **SDKs**

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging SDKs along with working examples, to get you started in no time.

## **SDK Examples**

{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetImageFeaturesFromSearchContext.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetImageFeaturesFromSearchContext.java" >}}

{{< /tab >}}

{{< /tabs >}}
