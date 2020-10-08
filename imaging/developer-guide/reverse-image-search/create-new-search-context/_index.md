---
title: "Create new Search Context"
type: docs
url: /create-new-search-context/
weight: 10
---

## **Introduction**

Search context is a special object which store features index structure and some service information in client session. Moreover, Features index is a data structure for fast image search. This article explains how to create new search context. [POST /imaging/ai/imageSearch/create](https://apireference.aspose.cloud/imaging/#/SearchContext/CreateImageSearch) API creates empty search context with certain settings.The search context state is stored in the storage as a file (searchContextId).search. Its key parameters description is given below:

**detector** - features detector (default AKAZE)

**matchingAlgorithm** – features matching algorithm (default RandomBinaryTree)

## **Resource URI**

[Swagger UI](https://apireference.aspose.cloud/imaging/#/SearchContext/CreateImageSearch) lets you call Aspose.Imaging REST APIs directly from the browser. The description of the APIs and there parameters are also given there.

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



// cURL example to create new search context

curl -v "https://api.aspose.cloud/v2/imaging/ai/imageSearch/create" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Content-Length: 0" \
-H "Authorization: Bearer <access_token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Id": "f0cf8f1f-6a96-420c-927d-f200757ffbb8",

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

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "CreateSearchContext.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "CreateNewSearchContext.java" >}}

{{< /tab >}}

{{< /tabs >}}
