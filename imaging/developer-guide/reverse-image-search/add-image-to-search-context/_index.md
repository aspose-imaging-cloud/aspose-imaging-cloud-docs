---
title: "Add Image to Search Context"
type: docs
url: /add-image-to-search-context/
weight: 150
---

## **Introduction**

This article explain how to add image and image features to search context. Image is stored in storage folder. The API URL is:

[POST /imaging/ai/imageSearch/{searchContextId}/image](https://apireference.aspose.cloud/imaging/#/SearchContextImages/AddSearchImage)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContextImages/AddSearchImage) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and their parameters are also given there.

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

// cURL example to add image to search context

curl -v "https://api.aspose.cloud/v3/imaging/ai/imageSearch/c5354cad-18c1-4af4-9444-69b23d891c67/image?imageId=aspose.jpg" \
-X POST \
-T aspose.jpg \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## **SDKs**

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging SDKs along with working examples, to get you started in no time.

## **SDK Examples**

{{< tabs tabTotal="1" tabID="4" tabName1="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "AddImageAndImagesFeaturesToSearchContext.java" >}}

{{< /tab >}}

{{< /tabs >}}
