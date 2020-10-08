---
title: "Get TIFF Frame Properties"
type: docs
url: /get-tiff-frame-properties/
weight: 30
---

## **Introduction**
This article explains how to retrieve properties of a specific Tiff Frame. The API accepts frame ID as an argument and returns properties of that TIFF frame.

The frame properties can be retrieved using one of the following two APIs:

- [GET /imaging/{name}/frames/{frameId}/properties](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrameProperties)
- [POST /imaging/frames/{frameId}/properties](https://apireference.aspose.cloud/imaging/#/Frames/ExtractImageFrameProperties)

The former API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrameProperties) you can call Aspose.Imaging REST APIs directly from the browser. Description of an API and its parameters are also provided there.
## **cURL Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to get properties of specific TIFF frame

curl -v "https://api.aspose.cloud/v3/imaging/SampleTiff.tiff/frames/1/properties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Height": 436,

  "Width": 419,

  "BitsPerPixel": 8,

  "BmpProperties": null,

  "GifProperties": null,

  "JpegProperties": null,

  "PngProperties": null,

  "TiffProperties": {

    "Frames": [

      {

        "FrameOptions": {

          "IsValid": true,

          "Artist": null,

          "ByteOrder": "LittleEndian",

          "BitsPerSample": [

            8

          ],

          "Compression": "Lzw",

          "Copyright": null,

          "ColorMap": [

            2570,

            3341,

            36751,

            16191,

            22616,

            22873,

            21074,

            37265,

            51400,

            34695,

            1542,

            2827,

            17733,

            37522,

            26471,

            46517,

            33667,

            39321,

            50372,

            3084,

            12336,

            42148,

            14649,

            46260,

            13621,

            33153,

            58339,

            19275,

            8738,

            28013,

            24158,

            23644,

            9509,

            44461,

            25186,

            1028,

            43433,

            3598,

            29555,

            17733,

            56026,

            16191,

            40092,

            4626,

            23130,

            46517,

            24672,

            55255,

            51914,

            53199,

            47031,

            2056,

            48316,

            35209,

            6682,

            55255,

            2570,

            15163,

            29298,

            33410,

            55512,

            28270,

            35980,

            31354,

            51143,

            57568,

            25700,

            20303,

            11822,

            47802,

            16191,

            54484,

            33410,

            2056,

            25443,

            37779,

            12336,

            57311,

            20817,

            9766,

            7196,

            37008,

            23130,

            30326,

            52685,

            43947,

            41120,

            12593,

            54741,

            58853,

            39064,

            51657,

            20817,

            38550,

            35209,

            35980,

            31868,

            56797,

            42919,

            18761,

            45232,

            5911,

            48316,

            27499,

            49858,

            57054,

            26214,

            38036,

            20817,

            25957,

            23130,

            17476,

            11308,

            6682,

            6939,

            62194,

            13621,

            21845,

            11308,

            55255,

            40606,

            33924,

            33924,

            53199,

            41891,

            26471,

            15934,

            51914,

            20560,

            48573,

            18247,

            1028,

            22873,

            34952,

            4883,

            31868,

            33924,

            50372,

            48830,

            63736,

            18504,

            37522,

            40092,

            44718,

            52942,

            51143,

            18761,

            1285,

            38550,

            22102,

            23901,

            41634,

            31868,

            30326,

            36751,

            15420,

            37779,

            15420,

            41891,

            22616,

            52171,

            25957,

            45232,

            23644,

            52942,

            48830,

            55769,

            42919,

            8224,

            53199,

            53456,

            43690,

            61937,

            43690,

            43433,

            21845,

            37265,

            35980,

            13107,

            18504,

            47545,

            37265,

            54484,

            37008,

            36751,

            46003,

            44204,

            45746,

            38293,

            50372,

            34438,

            24158,

            23130,

            40863,

            17990,

            38293,

            27756,

            41634,

            61680,

            16448,

            32382,

            3341,

            20303,

            8738,

            13621,

            10280,

            42148,

            60138,

            25443,

            62451,

            15163,

            52171,

            21331,

            24158,

            18247,

            22102,

            49344,

            41891,

            44204,

            32896,

            43176,

            21588,

            7710,

            27242,

            30069,

            26471,

            29555,

            51143,

            41377,

            55255,

            40606,

            34438,

            56283,

            29812,

            57825,

            28527,

            38807,

            34952,

            27756,

            4626,

            33667,

            44461,

            28013,

            6168,

            47031,

            9766,

            51657,

            12336,

            34438,

            35209,

            40092,

            59624,

            27756,

            60652,

            63479,

            61937,

            1542,

            34181,

            36237,

            17733,

            50629,

            47288,

            19532,

            33410,

            52171,

            2056,

            10280,

            26214,

            35723,

            59110,

            20817,

            51400,

            43690,

            35466,

            59624,

            18761,

            11051,

            42919,

            41377,

            51143,

            3855,

            41891,

            58339,

            11051,

            39064,

            26985,

            19275,

            1028,

            27756,

            45232,

            25700,

            13364,

            9509,

            22359,

            28784,

            33924,

            62965,

            27242,

            46774,

            5911,

            41377,

            55512,

            35209,

            58596,

            2827,

            42405,

            54998,

            31097,

            41634,

            34952,

            34952,

            46774,

            10794,

            30840,

            55255,

            41891,

            59110,

            41634,

            3598,

            31097,

            55255,

            64764,

            38550,

            18761,

            21845,

            47288,

            17990,

            62708,

            44204,

            14649,

            47545,

            37779,

            26214,

            59624,

            10794,

            6682,

            37008,

            38550,

            5911,

            26985,

            51400,

            62708,

            27499,

            1542,

            54998,

            54998,

            51657,

            51657,

            31611,

            35466,

            5397,

            29298,

            31097,

            56797,

            43690,

            39064,

            47545,

            26985,

            17990,

            26985,

            47802,

            56026,

            23130,

            9509,

            21845,

            23901,

            22359,

            37008,

            10280,

            31611,

            23644,

            64764,

            14135,

            43947,

            10023,

            54484,

            39321,

            30840,

            47031,

            51400,

            47288,

            24672,

            44461,

            41634,

            30840,

            9509,

            14649,

            21845,

            3855,

            30326,

            15420,

            15934,

            46774,

            44975,

            39064,

            63993,

            15163,

            38036,

            24158,

            38036,

            49087,

            5911,

            15163,

            17476,

            55255,

            19018,

            21588,

            61680,

            44718,

            31354,

            50629,

            14649,

            12850,

            38807,

            38550,

            10280,

            65021,

            6425,

            41891,

            23387,

            47031,

            48316,

            51657,

            38807,

            6939,

            44718,

            45489,

            2313,

            59881,

            6168,

            13621,

            19018,

            54998,

            16962,

            23130,

            17990,

            47802,

            23387,

            48830,

            6682,

            50372,

            58596,

            41634,

            44204,

            34438,

            52942,

            34181,

            2313,

            5911,

            11051,

            15163,

            31611,

            38550,

            30840,

            58082,

            17733,

            18247,

            36494,

            50115,

            41634,

            14135,

            30069,

            34695,

            60138,

            44718,

            63736,

            14135,

            59367,

            26985,

            22359,

            34438,

            41891,

            45489,

            41634,

            44718,

            23644,

            35723,

            20046,

            19789,

            10280,

            29298,

            36237,

            26471,

            63222,

            28270,

            55512,

            39578,

            31354,

            9252,

            13878,

            5654,

            14392,

            9252,

            47802,

            7710,

            3084,

            2313,

            50886,

            26471,

            5397,

            47031,

            6682,

            51657,

            2056,

            5911,

            47288,

            3598,

            58596,

            51400,

            59624,

            64507,

            60909,

            1799,

            21074,

            40863,

            2313,

            40349,

            37265,

            22102,

            12593,

            54998,

            1799,

            4112,

            15163,

            30069,

            50629,

            23387,

            41634,

            40606,

            26985,

            55255,

            12336,

            14392,

            41377,

            31097,

            50115,

            9252,

            30583,

            57311,

            4883,

            26728,

            24672,

            12850,

            1542,

            21588,

            48573,

            6425,

            4883,

            3855,

            14392,

            32896,

            23387,

            58339,

            22359,

            41891,

            2056,

            32896,

            50886,

            30583,

            46260,

            1542,

            28527,

            44461,

            19018,

            17733,

            36751,

            24158,

            21588,

            7967,

            23901,

            44975,

            37008,

            49858,

            36237,

            9509,

            24415,

            55512,

            62451,

            32382,

            4112,

            15163,

            41120,

            14649,

            51143,

            37522,

            8995,

            40349,

            41891,

            19275,

            61166,

            15420,

            1799,

            25186,

            36751,

            2056,

            14392,

            41120,

            55255,

            32382,

            1542,

            51657,

            36494,

            46774,

            50886,

            28013,

            20560,

            1542,

            23644,

            34181,

            60909,

            44975,

            27756,

            49344,

            18247,

            23644,

            29298,

            30840,

            56026,

            12850,

            12079,

            4369,

            24415,

            23644,

            27242,

            2570,

            22102,

            17733,

            63736,

            9766,

            33667,

            10280,

            41891,

            41377,

            14392,

            41120,

            33153,

            45232,

            28527,

            33667,

            20560,

            25443,

            3598,

            4369,

            8738,

            10537,

            10537,

            13364,

            19532\*Connection#0tohostapi.aspose.cloudleftintact,

            32896,

            35723,

            20560,

            44975,

            15163,

            29298,

            29041,

            16962,

            31868,

            2056,

            8995,

            8995,

            48573,

            7967,

            19275,

            51657,

            31868,

            29298,

            43690,

            19532,

            7196,

            30069,

            21588,

            10280,

            61166,

            10537,

            22873,

            27756,

            26728,

            49601,

            37265,

            28270,

            9766,

            21845,

            26214,

            1028,

            40863,

            2313,

            16191,

            18761,

            46260,

            5140,

            18504,

            18504,

            37779,

            13364,

            37008,

            11051,

            37522,

            51914,

            27756,

            28013,

            16962,

            59624,

            31354,

            5911,

            6682,

            15677,

            18504,

            24158,

            36237,

            34438,

            37522,

            7710,

            8995,

            21588,

            38036,

            27499,

            2313,

            19532,

            37522,

            49601,

            36751,

            51657,

            16448,

            59110,

            25957,

            8224,

            26985,

            27242,

            30069,

            36751,

            36751,

            18504,

            40349,

            25957,

            15420,

            4369,

            35980,

            33924,

            17990,

            57568,

            29812,

            45232,

            44718,

            18247,

            4369,

            5140,

            2056,

            7967,

            9252,

            37265,

            14392,

            5140,

            6425,

            46003,

            10537,

            6168,

            45489,

            6425,

            45489,

            6168,

            6168,

            44718,

            7196,

            46260,

            42148,

            58596,

            55769,

            60909

          ],

          "DateTime": null,

          "DocumentName": null,

          "AlphaStorage": "Unspecified",

          "FillOrder": "Msb2Lsb",

          "HalfToneHints": null,

          "ImageDescription": null,

          "InkNames": null,

          "ScannerManufacturer": null,

          "MaxSampleValue": [

            255

          ],

          "MinSampleValue": [

            0

          ],

          "ScannerModel": null,

          "PageName": null,

          "Orientation": "TopLeft",

          "PageNumber": null,

          "Photometric": "Palette",

          "PlanarConfiguration": "Contiguous",

          "ResolutionUnit": "Inch",

          "RowsPerStrip": 31,

          "SampleFormat": [

            "Uint"

          ],

          "SamplesPerPixel": 1,

          "SmaxSampleValue": [

            4294967295

          ],

          "SminSampleValue": [

            0

          ],

          "SoftwareType": null,

          "StripByteCounts": [

            3193,

            2559,

            8269,

            7845,

            8773,

            8595,

            8542,

            6235,

            485

          ],

          "StripOffsets": [

            106558,

            109751,

            112310,

            120579,

            128424,

            137197,

            145792,

            154334,

            160569

          ],

          "SubFileType": "FileTypeDefault",

          "TargetPrinter": null,

          "Threshholding": "NoDithering",

          "TotalPages": 0,

          "Xposition": 0.0,

          "Xresolution": 96.0,

          "Yposition": 0.0,

          "Yresolution": 96.0,

          "FaxT4Options": "Encoding1D",

          "Predictor": "None",

          "ImageLength": 250,

          "ImageWidth": 385,

          "ValidTagCount": 15,

          "BitsPerPixel": 8

        },

        "Height": 250,

        "Width": 385,

        "ExifData": null

      }

    ],

    "ByteOrder": "LittleEndian",

    "ExifData": null

  },

  "PsdProperties": null,

  "DjvuProperties": null,

  "WebPProperties": null,

  "Jpeg2000Properties": null,

  "DicomProperties": null,

  "DngProperties": null,

  "OdgProperties": null,

  "HorizontalResolution": 96.0,

  "VerticalResolution": 96.0,

  "IsCached": false,

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to get properties of specific TIFF frame

curl -v "https://api.aspose.cloud/v3/imaging/frames/1/properties" \
-X POST \
-T SampleTiff.tiff \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Height": 436,

  "Width": 419,

  "BitsPerPixel": 8,

  "BmpProperties": null,

  "GifProperties": null,

  "JpegProperties": null,

  "PngProperties": null,

  "TiffProperties": {

    "Frames": [

      {

        "FrameOptions": {

          "IsValid": true,

          "Artist": null,

          "ByteOrder": "LittleEndian",

          "BitsPerSample": [

            8

          ],

          "Compression": "Lzw",

          "Copyright": null,

          "ColorMap": [

            2570,

            3341,

            36751,

            16191,

            22616,

            22873,

            21074,

            37265,

            51400,

            34695,

            1542,

            2827,

            17733,

            37522,

            26471,

            46517,

            33667,

            39321,

            50372,

            3084,

            12336,

            42148,

            14649,

            46260,

            13621,

            33153,

            58339,

            19275,

            8738,

            28013,

            24158,

            23644,

            9509,

            44461,

            25186,

            1028,

            43433,

            3598,

            29555,

            17733,

            56026,

            16191,

            40092,

            4626,

            23130,

            46517,

            24672,

            55255,

            51914,

            53199,

            47031,

            2056,

            48316,

            35209,

            6682,

            55255,

            2570,

            15163,

            29298,

            33410,

            55512,

            28270,

            35980,

            31354,

            51143,

            57568,

            25700,

            20303,

            11822,

            47802,

            16191,

            54484,

            33410,

            2056,

            25443,

            37779,

            12336,

            57311,

            20817,

            9766,

            7196,

            37008,

            23130,

            30326,

            52685,

            43947,

            41120,

            12593,

            54741,

            58853,

            39064,

            51657,

            20817,

            38550,

            35209,

            35980,

            31868,

            56797,

            42919,

            18761,

            45232,

            5911,

            48316,

            27499,

            49858,

            57054,

            26214,

            38036,

            20817,

            25957,

            23130,

            17476,

            11308,

            6682,

            6939,

            62194,

            13621,

            21845,

            11308,

            55255,

            40606,

            33924,

            33924,

            53199,

            41891,

            26471,

            15934,

            51914,

            20560,

            48573,

            18247,

            1028,

            22873,

            34952,

            4883,

            31868,

            33924,

            50372,

            48830,

            63736,

            18504,

            37522,

            40092,

            44718,

            52942,

            51143,

            18761,

            1285,

            38550,

            22102,

            23901,

            41634,

            31868,

            30326,

            36751,

            15420,

            37779,

            15420,

            41891,

            22616,

            52171,

            25957,

            45232,

            23644,

            52942,

            48830,

            55769,

            42919,

            8224,

            53199,

            53456,

            43690,

            61937,

            43690,

            43433,

            21845,

            37265,

            35980,

            13107,

            18504,

            47545,

            37265,

            54484,

            37008,

            36751,

            46003,

            44204,

            45746,

            38293,

            50372,

            34438,

            24158,

            23130,

            40863,

            17990,

            38293,

            27756,

            41634,

            61680,

            16448,

            32382,

            3341,

            20303,

            8738,

            13621,

            10280,

            42148,

            60138,

            25443,

            62451,

            15163,

            52171,

            21331,

            24158,

            18247,

            22102,

            49344,

            41891,

            44204,

            32896,

            43176,

            21588,

            7710,

            27242,

            30069,

            26471,

            29555,

            51143,

            41377,

            55255,

            40606,

            34438,

            56283,

            29812,

            57825,

            28527,

            38807,

            34952,

            27756,

            4626,

            33667,

            44461,

            28013,

            6168,

            47031,

            9766,

            51657,

            12336,

            34438,

            35209,

            40092,

            59624,

            27756,

            60652,

            63479,

            61937,

            1542,

            34181,

            36237,

            17733,

            50629,

            47288,

            19532,

            33410,

            52171,

            2056,

            10280,

            26214,

            35723,

            59110,

            20817,

            51400,

            43690,

            35466,

            59624,

            18761,

            11051,

            42919,

            41377,

            51143,

            3855,

            41891,

            58339,

            11051,

            39064,

            26985,

            19275,

            1028,

            27756,

            45232,

            25700,

            13364,

            9509,

            22359,

            28784,

            33924,

            62965,

            27242,

            46774,

            5911,

            41377,

            55512,

            35209,

            58596,

            2827,

            42405,

            54998,

            31097,

            41634,

            34952,

            34952,

            46774,

            10794,

            30840,

            55255,

            41891,

            59110,

            41634,

            3598,

            31097,

            55255,

            64764,

            38550,

            18761,

            21845,

            47288,

            17990,

            62708,

            44204,

            14649,

            47545,

            37779,

            26214,

            59624,

            10794,

            6682,

            37008,

            38550,

            5911,

            26985,

            51400,

            62708,

            27499,

            1542,

            54998,

            54998,

            51657,

            51657,

            31611,

            35466,

            5397,

            29298,

            31097,

            56797,

            43690,

            39064,

            47545,

            26985,

            17990,

            26985,

            47802,

            56026,

            23130,

            9509,

            21845,

            23901,

            22359,

            37008,

            10280,

            31611,

            23644,

            64764,

            14135,

            43947,

            10023,

            54484,

            39321,

            30840,

            47031,

            51400,

            47288,

            24672,

            44461,

            41634,

            30840,

            9509,

            14649,

            21845,

            3855,

            30326,

            15420,

            15934,

            46774,

            44975,

            39064,

            63993,

            15163,

            38036,

            24158,

            38036,

            49087,

            5911,

            15163,

            17476,

            55255,

            19018,

            21588,

            61680,

            44718,

            31354,

            50629,

            14649,

            12850,

            38807,

            38550,

            10280,

            65021,

            6425,

            41891,

            23387,

            47031,

            48316,

            51657,

            38807,

            6939,

            44718,

            45489,

            2313,

            59881,

            6168,

            13621,

            19018,

            54998,

            16962,

            23130,

            17990,

            47802,

            23387,

            48830,

            6682,

            50372,

            58596,

            41634,

            44204,

            34438,

            52942,

            34181,

            2313,

            5911,

            11051,

            15163,

            31611,

            38550,

            30840,

            58082,

            17733,

            18247,

            36494,

            50115,

            41634,

            14135,

            30069,

            34695,

            60138,

            44718,

            63736,

            14135,

            59367,

            26985,

            22359,

            34438,

            41891,

            45489,

            41634,

            44718,

            23644,

            35723,

            20046,

            19789,

            10280,

            29298,

            36237,

            26471,

            63222,

            28270,

            55512,

            39578,

            31354,

            9252,

            13878,

            5654,

            14392,

            9252,

            47802,

            7710,

            3084,

            2313,

            50886,

            26471,

            5397,

            47031,

            6682,

            51657,

            2056,

            5911,

            47288,

            3598,

            58596,

            51400,

            59624,

            64507,

            60909,

            1799,

            21074,

            40863,

            2313,

            40349,

            37265,

            22102,

            12593,

            54998,

            1799,

            4112,

            15163,

            30069,

            50629,

            23387,

            41634,

            40606,

            26985,

            55255,

            12336,

            14392,

            41377,

            31097,

            50115,

            9252,

            30583,

            57311,

            4883,

            26728,

            24672,

            12850,

            1542,

            21588,

            48573,

            6425,

            4883,

            3855,

            14392,

            32896,

            23387,

            58339,

            22359,

            41891,

            2056,

            32896,

            50886,

            30583,

            46260,

            1542,

            28527,

            44461,

            19018,

            17733,

            36751,

            24158,

            21588,

            7967,

            23901,

            44975,

            37008,

            49858,

            36237,

            9509,

            24415,

            55512,

            62451,

            32382,

            4112,

            15163,

            41120,

            14649,

            51143,

            37522,

            8995,

            40349,

            41891,

            19275,

            61166,

            15420,

            1799,

            25186,

            36751,

            2056,

            14392,

            41120,

            55255,

            32382,

            1542,

            51657,

            36494,

            46774,

            50886,

            28013,

            20560,

            1542,

            23644,

            34181,

            60909,

            44975,

            27756,

            49344,

            18247,

            23644,

            29298,

            30840,

            56026,

            12850,

            12079,

            4369,

            24415,

            23644,

            27242,

            2570,

            22102,

            17733,

            63736,

            9766,

            33667,

            10280,

            41891,

            41377,

            14392,

            41120,

            33153,

            45232,

            28527,

            33667,

            20560,

            25443,

            3598,

            4369,

            8738,

            10537,

            10537,

            13364,

            19532\*Connection#0tohostapi.aspose.cloudleftintact,

            32896,

            35723,

            20560,

            44975,

            15163,

            29298,

            29041,

            16962,

            31868,

            2056,

            8995,

            8995,

            48573,

            7967,

            19275,

            51657,

            31868,

            29298,

            43690,

            19532,

            7196,

            30069,

            21588,

            10280,

            61166,

            10537,

            22873,

            27756,

            26728,

            49601,

            37265,

            28270,

            9766,

            21845,

            26214,

            1028,

            40863,

            2313,

            16191,

            18761,

            46260,

            5140,

            18504,

            18504,

            37779,

            13364,

            37008,

            11051,

            37522,

            51914,

            27756,

            28013,

            16962,

            59624,

            31354,

            5911,

            6682,

            15677,

            18504,

            24158,

            36237,

            34438,

            37522,

            7710,

            8995,

            21588,

            38036,

            27499,

            2313,

            19532,

            37522,

            49601,

            36751,

            51657,

            16448,

            59110,

            25957,

            8224,

            26985,

            27242,

            30069,

            36751,

            36751,

            18504,

            40349,

            25957,

            15420,

            4369,

            35980,

            33924,

            17990,

            57568,

            29812,

            45232,

            44718,

            18247,

            4369,

            5140,

            2056,

            7967,

            9252,

            37265,

            14392,

            5140,

            6425,

            46003,

            10537,

            6168,

            45489,

            6425,

            45489,

            6168,

            6168,

            44718,

            7196,

            46260,

            42148,

            58596,

            55769,

            60909

          ],

          "DateTime": null,

          "DocumentName": null,

          "AlphaStorage": "Unspecified",

          "FillOrder": "Msb2Lsb",

          "HalfToneHints": null,

          "ImageDescription": null,

          "InkNames": null,

          "ScannerManufacturer": null,

          "MaxSampleValue": [

            255

          ],

          "MinSampleValue": [

            0

          ],

          "ScannerModel": null,

          "PageName": null,

          "Orientation": "TopLeft",

          "PageNumber": null,

          "Photometric": "Palette",

          "PlanarConfiguration": "Contiguous",

          "ResolutionUnit": "Inch",

          "RowsPerStrip": 31,

          "SampleFormat": [

            "Uint"

          ],

          "SamplesPerPixel": 1,

          "SmaxSampleValue": [

            4294967295

          ],

          "SminSampleValue": [

            0

          ],

          "SoftwareType": null,

          "StripByteCounts": [

            3193,

            2559,

            8269,

            7845,

            8773,

            8595,

            8542,

            6235,

            485

          ],

          "StripOffsets": [

            106558,

            109751,

            112310,

            120579,

            128424,

            137197,

            145792,

            154334,

            160569

          ],

          "SubFileType": "FileTypeDefault",

          "TargetPrinter": null,

          "Threshholding": "NoDithering",

          "TotalPages": 0,

          "Xposition": 0.0,

          "Xresolution": 96.0,

          "Yposition": 0.0,

          "Yresolution": 96.0,

          "FaxT4Options": "Encoding1D",

          "Predictor": "None",

          "ImageLength": 250,

          "ImageWidth": 385,

          "ValidTagCount": 15,

          "BitsPerPixel": 8

        },

        "Height": 250,

        "Width": 385,

        "ExifData": null

      }

    ],

    "ByteOrder": "LittleEndian",

    "ExifData": null

  },

  "PsdProperties": null,

  "DjvuProperties": null,

  "WebPProperties": null,

  "Jpeg2000Properties": null,

  "DicomProperties": null,

  "DngProperties": null,

  "OdgProperties": null,

  "HorizontalResolution": 96.0,

  "VerticalResolution": 96.0,

  "IsCached": false,

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetFramePropertiesOfTIFFImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetFramePropertiesOfTIFFImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetFramePropertiesOfTIFFImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetFramePropertiesOfTIFFImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}