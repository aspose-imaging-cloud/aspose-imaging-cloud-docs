---
title: "Get Search Context Status"
type: docs
url: /get-search-context-status/
weight: 20
---

## **Introduction**

This article explain how to get the current status of search context. It could be Idle, ExtractingFeatures, MatchingFeatures or Searching. If search context with a certain ID does not exist, the API returns error code and message. The API URL is:

[GET /imaging/ai/imageSearch/{searchContextId}/status](https://apireference.aspose.cloud/imaging/#/SearchContext/GetImageSearchStatus)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContext/GetImageSearchStatus) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and there parameters are also given there.

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

// cURL example to get the search context status

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/76901fe6-1427-4112-9fa2-8261cca7524a/status" \
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

  "Id": "76901fe6-1427-4112-9fa2-8261cca7524a",

  "SearchStatus": "Idle",

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## **SDKs**

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging SDKs along with working examples, to get you started in no time.

## **SDK Examples**

{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetTheSearchContextStatus.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetTheSearchContextStatus.java" >}}

{{< /tab >}}

{{< /tabs >}}
