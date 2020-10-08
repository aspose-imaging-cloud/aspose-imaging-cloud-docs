---
title: "Extract Images Features and Add Them to Search Context"
type: docs
url: /extract-images-features-and-add-them-to-search-context/
weight: 100
---

# **Introduction**

This article explain how to extract features from image sources (storage, url or/and features collection) and add them to features index. The API URL is:

[POST /imaging/ai/imageSearch/{searchContextId}/features](https://apireference.aspose.cloud/imaging/#/SearchContextFeatures/CreateImageFeatures)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContextFeatures/CreateImageFeatures) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and their parameters are also given there.

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

// cURL example to extract image features and add them to search context

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/c5354cad-18c1-4af4-9444-69b23d891c67/features" \
-X POST \
-T aspose.jpg \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <access_token>"

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

{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "AddImageFeaturesToSearchContext.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "ExtractImageFeaturesAndAddThemToSearchContext.java" >}}

{{< /tab >}}

{{< /tabs >}}
