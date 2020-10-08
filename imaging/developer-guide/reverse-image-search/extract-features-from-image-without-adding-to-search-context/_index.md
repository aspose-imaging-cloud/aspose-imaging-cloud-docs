---
title: "Extract Features from Image without Adding to Search Context"
type: docs
url: /extract-features-from-image-without-adding-to-search-context/
weight: 40
---

## **Introduction**

This article explain how to extract features from image without adding to search context. The API URL is:

[GET /imaging/ai/imageSearch/{searchContextId}/image2features](https://apireference.aspose.cloud/imaging/#/SearchContext/ExtractImageFeatures)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContext/ExtractImageFeatures) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and there parameters are also given there.

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

// cURL example to extract features from image without adding to search context

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/76972fff-461b-42d2-8bf4-814a729943bf/image2features?imageId=aspose.jpg" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Content-Length: 0" \
-H "Authorization: Bearer <access_token>" 

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "ImageId": "aspose.jpg",

  "FeaturesCount": 508,

  "FeatureLengthInBits": 488,

  "Features": "ot6WQAEAAAAAAAAAlVD6OoeptkDV2K9CpC8qQj0AAAD...",

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## **SDKs**

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging SDKs along with working examples, to get you started in no time.

## **SDK Examples**

{{< tabs tabTotal="1" tabID="4" tabName1="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "ExtractFeaturesFromImageWithoutAddingToSearchContext.java" >}}

{{< /tab >}}

{{< /tabs >}}
