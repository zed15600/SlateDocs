# Ads

## Get All Ads

```shell
curl "https://admin.austin.ownlocal.com/api/v1/ads" \
  -H "Authorization: <token>"
```

> The above command returns JSON structured like this:

```json
[
  {
    "adUuid": "795d064b-1810-4f6b-bada-6a9f7d534579",
    "fileName": "{original_filename}.pdf",
    "adCustomId": "234567",
    "businessUuid": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
    "publisherUuid": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
    "image": "https://assets.ownlocal.com/ads/795d064b-1810-4f6b-bada-6a9f7d534579/order_image.jpeg",
    "startDate": "2019-09-01",
    "endDate": "2019-09-30",
    "dateModified": "2019-09-03",
    "dateCreated": "2019-09-03",
    "adText": "string",
    "offerCount": "4",
    "offers": [
      {
        "offerUuid": "bbfdc747-b2c9-4232-be7a-81dbf5290af4",
        "offerImage": "https://ownlocal.imgix.net/offers/bbfdc747-b2c9-4232-be7a-81dbf5290af4.png",
        "title": "40% Off Full Interior Detail Package",
        "description": "",
        "originalPrice": "",
        "discountPercentage": "",
        "discountPrice": "",
        "discountOff": "",
        "newPrice": "",
        "bogo": false,
        "free": false,
        "validThrough": "",
        "gtin8": [
          {
            "class": 77015300
          },
          {
            "class": 77015301
          }
        ]
      },
      {
        "offerUuid": "5faaff6a-5ad9-4fcf-b68d-a025b1badd29",
        "offerImage": "https://ownlocal.imgix.net/offers/5faaff6a-5ad9-4fcf-b68d-a025b1badd29.png",
        "title": "Free Brake Inspection with Every Oil Change",
        "description": "",
        "originalPrice": "",
        "discountPercentage": "",
        "discountPrice": "",
        "discountOff": "",
        "newPrice": "",
        "bogo": false,
        "free": false,
        "validThrough": "",
        "gtin8": [
          {
            "class": 77015300
          },
          {
            "class": 77015301
          }
        ]
      },
      {
        "offerUuid": "2df8c96b-f565-4c77-b776-8b02a9a92d30",
        "offerImage": "https://ownlocal.imgix.net/offers/2df8c96b-f565-4c77-b776-8b02a9a92d30.png",
        "title": "20% Off Full Vehicle Tint",
        "description": "",
        "originalPrice": "",
        "discountPercentage": "",
        "discountPrice": "",
        "discountOff": "",
        "newPrice": "",
        "bogo": false,
        "free": false,
        "validThrough": "",
        "gtin8": [
          {
            "class": 77011700
          },
          {
            "class": 77011701
          }
        ]
      },
      {
        "offerUuid": "fea2a6e0-7993-460a-9a54-88acf6dc479b",
        "offerImage": "https://ownlocal.imgix.net/offers/fea2a6e0-7993-460a-9a54-88acf6dc479b.png",
        "title": "$150 Off Windshield Replacement (when going through Insurance)",
        "description": "",
        "originalPrice": "",
        "discountPercentage": "",
        "discountPrice": "",
        "discountOff": "",
        "newPrice": "",
        "bogo": false,
        "free": false,
        "validThrough": "",
        "gtin8": [
          {
            "class": 77011300
          },
          {
            "class": 77011301
          }
        ]
      }
    ]
  }
]
```

This endpoint retrieves all ads.

### HTTP Request

`GET https://admin.austin.ownlocal.com/api/v1/ads`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
categories | string array | Lists ads from business belonging to those categories
subCategories | string array | Lists ads from business belonging to those sub categories
offerCountMin | integer | Lists ads with offers count is greater or equal than the value provided
offerCountMax | integer | Lists ads with offers count is lesser or equal than the value provided
startDateMin | date | Lists ads with start date after or equal to the provided value
startDateMax | date | Lists ads with start date before or equal to the provided value
endDateMin | date | Lists ads with end date after or equal to the provided value
endDateMax | date | Lists ads with end date before or equal to the provided value
dateModifiedMin | date | Lists ads modified that day or after
dateModifiedMax | date | Lists ads modified that day or before
dateCreatedMin | date | Lists ads created that day or after
dateCreatedMax | date | Lists ads created that day or before
businessUuids | string array | Lists ads belonging to the specified businesses
publisherUuids | string array | Lists ads published by the specified partners
sortedBy | string | Specifies the sorting order
size | integer | Specifies the response size in ads amount (default: 20)
page | integer | Specifies the page to retrieve based in the size parameter (default: 1)

## Create an Ad

```shell
curl -X POST "https://admin.austin.ownlocal.com/api/v1/ads" \
  -H "Authorization: <token>" \
  -d "{
    'publisherUuid': '7e6ffeb2-22f3-4869-b189-d202996814cf',
    'businessUuid': '69271d95-e891-4bf7-a9ba-ce249e36e236',
    'adCustomId': '234567',
    'startDate': '2019-08-23',
    'endDate': '2019-09-23'
  }"
```

This endpoint creates an ad.

### HTTP Request

`POST https://admin.austin.ownlocal.com/api/v1/ads`

### Body Parameters

Parameter | Type | Description
--- | --- | ---
publisherUuid | string | The publisher under which this ad is going to be published
businessUuid | string | The business which this ad belongs to
adCustomId | string | A custom identifier for the ad
startDate | date | The offer start date
endDate | date | The offer end date

## Get a Specific Ad

```shell
curl "https://admin.austin.ownlocal.com/api/v1/ads/795d064b-1810-4f6b-bada-6a9f7d534579" \
  -H "Authorization: <token>"
```

> The above command returns JSON structured like this:

```json
{
  "adUuid": "795d064b-1810-4f6b-bada-6a9f7d534579",
  "fileName": "{original_filename}.pdf",
  "adCustomId": "234567",
  "businessUuid": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "publisherUuid": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "image": "https://assets.ownlocal.com/ads/795d064b-1810-4f6b-bada-6a9f7d534579/order_image.jpeg",
  "startDate": "2019-09-01",
  "endDate": "2019-09-30",
  "dateModified": "2019-09-03",
  "dateCreated": "2019-09-03",
  "adText": "string",
  "offerCount": "4",
  "offers": [
    {
      "offerUuid": "bbfdc747-b2c9-4232-be7a-81dbf5290af4",
      "offerImage": "https://ownlocal.imgix.net/offers/bbfdc747-b2c9-4232-be7a-81dbf5290af4.png",
      "title": "40% Off Full Interior Detail Package",
      "description": "",
      "originalPrice": "",
      "discountPercentage": "",
      "discountPrice": "",
      "discountOff": "",
      "newPrice": "",
      "bogo": false,
      "free": false,
      "validThrough": "",
      "gtin8": [
        {
          "class": 77015300
        },
        {
          "class": 77015301
        }
      ]
    },
    {
      "offerUuid": "5faaff6a-5ad9-4fcf-b68d-a025b1badd29",
      "offerImage": "https://ownlocal.imgix.net/offers/5faaff6a-5ad9-4fcf-b68d-a025b1badd29.png",
      "title": "Free Brake Inspection with Every Oil Change",
      "description": "",
      "originalPrice": "",
      "discountPercentage": "",
      "discountPrice": "",
      "discountOff": "",
      "newPrice": "",
      "bogo": false,
      "free": false,
      "validThrough": "",
      "gtin8": [
        {
          "class": 77015300
        },
        {
          "class": 77015301
        }
      ]
    },
    {
      "offerUuid": "2df8c96b-f565-4c77-b776-8b02a9a92d30",
      "offerImage": "https://ownlocal.imgix.net/offers/2df8c96b-f565-4c77-b776-8b02a9a92d30.png",
      "title": "20% Off Full Vehicle Tint",
      "description": "",
      "originalPrice": "",
      "discountPercentage": "",
      "discountPrice": "",
      "discountOff": "",
      "newPrice": "",
      "bogo": false,
      "free": false,
      "validThrough": "",
      "gtin8": [
        {
          "class": 77011700
        },
        {
          "class": 77011701
        }
      ]
    },
    {
      "offerUuid": "fea2a6e0-7993-460a-9a54-88acf6dc479b",
      "offerImage": "https://ownlocal.imgix.net/offers/fea2a6e0-7993-460a-9a54-88acf6dc479b.png",
      "title": "$150 Off Windshield Replacement (when going through Insurance)",
      "description": "",
      "originalPrice": "",
      "discountPercentage": "",
      "discountPrice": "",
      "discountOff": "",
      "newPrice": "",
      "bogo": false,
      "free": false,
      "validThrough": "",
      "gtin8": [
        {
          "class": 77011300
        },
        {
          "class": 77011301
        }
      ]
    }
  ]
}
```

This endpoint retrieves a specific ad.

### HTTP Request

`GET http://admin.austin.ownlocal.com/api/v1/ads/<uuid>`

### URL Parameters

Parameter | Description
--------- | -----------
uuid | The uuid of the ad to retrieve

## Update an Ad

```shell
curl -X PATCH "https://admin.austin.ownlocal.com/api/v1/ads/<uuid>" \
  -H "Authorization: <token>" \
  -d "{
    'adUuid': '795d064b-1810-4f6b-bada-6a9f7d534579',
    'fileName': 'original_filename.pdf',
    'adCustomId': '234567',
    'businessUuid': '2db5e240-c098-4d59-b3a3-bc7b7abc2c4c',
    'publisherUuid': '2db5e240-c098-4d59-b3a3-bc7b7abc2c4c',
    'image': 'https://assets.ownlocal.com/ads/795d064b-1810-4f6b-bada-6a9f7d534579/order_image.jpeg',
    'startDate': '2019-09-01',
    'endDate': '2019-09-30',
    'dateModified': '2019-09-03',
    'dateCreated': '2019-09-03',
    'adText': 'string',
    'offerCount': '4',
    'offers': [
      {
        'offerUuid': 'bbfdc747-b2c9-4232-be7a-81dbf5290af4',
        'offerImage': 'https://ownlocal.imgix.net/offers/bbfdc747-b2c9-4232-be7a-81dbf5290af4.png',
        'title': '40% Off Full Interior Detail Package',
        'description': '',
        'originalPrice': '',
        'discountPercentage': '',
        'discountPrice': '',
        'discountOff': '',
        'newPrice': '',
        'bogo': false,
        'free': false,
        'validThrough': '',
        'gtin8': [
          {
            'class': 77015300
          },
          {
            'class': 77015301
          }
        ]
      },
      {
        'offerUuid': '5faaff6a-5ad9-4fcf-b68d-a025b1badd29',
        'offerImage': 'https://ownlocal.imgix.net/offers/5faaff6a-5ad9-4fcf-b68d-a025b1badd29.png',
        'title': 'Free Brake Inspection with Every Oil Change',
        'description': '',
        'originalPrice': '',
        'discountPercentage': '',
        'discountPrice': '',
        'discountOff': '',
        'newPrice': '',
        'bogo': false,
        'free': false,
        'validThrough': '',
        'gtin8': [
          {
            'class': 77015300
          },
          {
            'class': 77015301
          }
        ]
      },
      {
        'offerUuid': '2df8c96b-f565-4c77-b776-8b02a9a92d30',
        'offerImage': 'https://ownlocal.imgix.net/offers/2df8c96b-f565-4c77-b776-8b02a9a92d30.png',
        'title': '20% Off Full Vehicle Tint',
        'description': '',
        'originalPrice': '',
        'discountPercentage': '',
        'discountPrice': '',
        'discountOff': '',
        'newPrice': '',
        'bogo': false,
        'free': false,
        'validThrough': '',
        'gtin8': [
          {
            'class': 77011700
          },
          {
            'class': 77011701
          }
        ]
      },
      {
        'offerUuid': 'fea2a6e0-7993-460a-9a54-88acf6dc479b',
        'offerImage': 'https://ownlocal.imgix.net/offers/fea2a6e0-7993-460a-9a54-88acf6dc479b.png',
        'title': '$150 Off Windshield Replacement (when going through Insurance)',
        'description': '',
        'originalPrice': '',
        'discountPercentage': '',
        'discountPrice': '',
        'discountOff': '',
        'newPrice': '',
        'bogo': false,
        'free': false,
        'validThrough': '',
        'gtin8': [
          {
            'class': 77011300
          },
          {
            'class': 77011301
          }
        ]
      }
    ]
  }"
```

Use this endpoint to update a specific ad data.

### HTTP Request

`PATCH https://admin.austin.ownlocal.com/api/v1/ads/<uuid>`

### URL Parameters

Parameter | Description
--- | ---
uuid | The ad to update's uuid

### Body Parameters

See models section.

## Upload Ad file

```shell
curl -X POST "https://admin.austin.ownlocal.com/api/v1/ads/<uuid>/content" \
  -H "Authorization: <token>" \
  -H "Content-Type: multipart/form-data" \
  -F "file=<file.pdf>;type=application/pdf" \
  -F "fileName=<file.pdf>
```

This endpoint uploads the PDF file for a specific ad

### URL Parameters

Parameter | Description
--- | ---
uuid | The ad's uuid for which the file will be updloaded

### Form Parameters

Parameter | Type | Description
--- | --- | ---
file | pdf | The ad file to upload
name | string | The name that the file should be stored as. must include extension
