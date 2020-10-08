---
title: "Find Images By Tags"
type: docs
url: /find-images-by-tags/
weight: 80
---

## **Introduction**

This article explains how to find images by tags.

The API URL is: [POST /imaging/ai/imageSearch/{searchContextId}/findByTags](https://apireference.aspose.cloud/imaging/#/SearchContext/FindImagesByTags)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContext/FindImagesByTags) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and their parameters are also given there.

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



// cURL example to find images by tags

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/cc435948-2dc3-4269-9299-052baa314d72/findByTags?similarityThreshold=90.0&maxCount=10" \
-X POST \
-d '["MyTag"]' \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <access_token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Results": [



  ],

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

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "FindSimilarImagesByTag.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "SearchImagesByTags.java" >}}

{{< /tab >}}

{{< /tabs >}}
