# Businesses

```shell
curl "https://admin.austin.ownlocal.com/api/v1/businesses" \
  -H "Authorization: <token>
```

> The above command returns JSON structured like this:

```json
[
  {
    "businessUuid": "69271d95-e891-4bf7-a9ba-ce249e36e236",
    "businessCustomId": "23456",
    "publisherUuids": [
      "e94df8d7-cc45-4ec9-b9fa-e42f04f74c38",
      "9103093d-596a-4ed4-a0ea-d7a5bfc35912"
    ],
    "name": "Cielo Azul Mexican Grill",
    "logoUrl": "http://www.cielobluemexreservations.com/CieloBlueMexicanGrill_logo.jpg",
    "website": "http://www.cielobluecantina.com",
    "urls": [
      {
        "url": "http://www.ciellobluemexreservations.com",
        "laber": "Reservations"
      }
    ],
    "description": "We provide our customers with a fun and happy environment along with our enthusiastic staff, always making sure our customers have the greatest time in our restaurants. We try to make everyone of our customers feel welcome, and to make them have a great experience with us.",
    "email": "generalmgr@cielobluecantina.com",
    "openingHours": "Mo,Tu,We,Th,Fr 09:00-12:00",
    "hoursGeneralDescription": "Open 6 days a week, Tuesday to Sunday",
    "conditionsOfAccess": "reservations accepted",
    "locations": [
      {
        "streetAddress": "197 Bloor St E",
        "addressLocality": "Oshawa",
        "addressRegion": "ON",
        "postalCode": "L1H 3M3",
        "telephones": [
          "905-720-2326"
        ]
      }
    ],
    "categories": [
      "Food and Beverage"
    ],
    "subCategories": [
      "Mexican Food"
    ],
    "social": {
      "facebookUrl": "https://www.facebook.com/CieloBlueBelmont/",
      "instagramUrl": "https://www.instagram.com/CieloBlueBelmont/",
      "twitterUrl": "https://www.twitter.com/CieloBlueBelmont/",
      "youtubeUrl": "https://www.youtube.com/CieloBlueBelmont/",
      "yelpUrl": "https://www.yelp.com/biz/Cielo-Blue-Belmont"
    },
    "acceptedPaymentMethods": [
      "MasterCard",
      "Cash"
    ],
    "images": [
      "https://assets.ownlocal.com/images/a78feabb-df16-4fde-87aa-fba233d71671.jpeg",
      "https://assets.ownlocal.com/images/bbfe0e1f-0d8a-40df-86bd-c6a2250c09ec.jpeg"
    ]
  }
]
```

This endpoint retrieves all businesses.

### HTTP Request

`GET https://admin.austin.ownlocal.com/api/v1/businesses`

### Query Parameters

Parameter | Type | Description
--- | --- | ---
categories | string array | Retrieves businesses belonging to those categories
subCategories | string array | Retrieves businesses belonging to those sub categories
dateModifiedMin | date | Retrieves businesses modified that day or after
dateModifiedMax | date | Retrieves businesses modified that day or before
dateCreatedMin | date | Retrieves businesses created that day or after
dateCreatedMax | date | Retrieves businesses created that day or before
publisherUuids | [string] array | Retrieves businesses listed in those partners
sortedBy | string | Specifies the sorting order
size | integer | Specifies the response size in businesses amount (default: 30)
page | integer | Specifies the page to retrieve based in the size parameter (default: 1)

## Create a Business

```shell
curl -X POST "https://admin.austin.ownlocal.com/api/v1/businesses" \
  -H "Authorization: <token>"
  -d "{
    'businessUuid': '69271d95-e891-4bf7-a9ba-ce249e36e236',
    'businessCustomId': '23456',
    'publisherUuids': [
      'e94df8d7-cc45-4ec9-b9fa-e42f04f74c38',
      '9103093d-596a-4ed4-a0ea-d7a5bfc35912'
    ],
    'name': 'Cielo Azul Mexican Grill',
    'logoUrl': 'http://www.cielobluemexreservations.com/CieloBlueMexicanGrill_logo.jpg',
    'website': 'http://www.cielobluecantina.com',
    'urls': [
      {
        'url': 'http://www.ciellobluemexreservations.com',
        'laber': 'Reservations'
      }
    ],
    'description': 'We provide our customers with a fun and happy environment along with our enthusiastic staff, always making sure our customers have the greatest time in our restaurants. We try to make everyone of our customers feel welcome, and to make them have a great experience with us.',
    'email': 'generalmgr@cielobluecantina.com',
    'openingHours': 'Mo,Tu,We,Th,Fr 09:00-12:00',
    'hoursGeneralDescription': 'Open 6 days a week, Tuesday to Sunday',
    'conditionsOfAccess': 'reservations accepted',
    'locations': [
      {
        'streetAddress': '197 Bloor St E',
        'addressLocality': 'Oshawa',
        'addressRegion': 'ON',
        'postalCode': 'L1H 3M3',
        'telephones': [
          '905-720-2326'
        ]
      }
    ],
    'categories': [
      'Food and Beverage'
    ],
    'subCategories': [
      'Mexican Food'
    ],
    'social': {
      'facebookUrl': 'https://www.facebook.com/CieloBlueBelmont/',
      'instagramUrl': 'https://www.instagram.com/CieloBlueBelmont/',
      'twitterUrl': 'https://www.twitter.com/CieloBlueBelmont/',
      'youtubeUrl': 'https://www.youtube.com/CieloBlueBelmont/',
      'yelpUrl': 'https://www.yelp.com/biz/Cielo-Blue-Belmont'
    },
    'acceptedPaymentMethods': [
      'MasterCard',
      'Cash'
    ],
    'images': [
      'https://assets.ownlocal.com/images/a78feabb-df16-4fde-87aa-fba233d71671.jpeg',
      'https://assets.ownlocal.com/images/bbfe0e1f-0d8a-40df-86bd-c6a2250c09ec.jpeg'
    ]
  }"
```

This endpoint creates a business.

### HTTP Request

`POST https://admin.austin.ownlocal.com`

### Body Parameters

See models section.

## Get a Specific Business

```shell
curl "https://admin.austin.ownlocal.com/api/v1/businesses/<uuid>" \
  -H "Authorization: <token>
```

> The above command returns JSON structured like this:

```json
{
  "businessUuid": "69271d95-e891-4bf7-a9ba-ce249e36e236",
  "businessCustomId": "23456",
  "publisherUuids": [
    "e94df8d7-cc45-4ec9-b9fa-e42f04f74c38",
    "9103093d-596a-4ed4-a0ea-d7a5bfc35912"
  ],
  "name": "Cielo Azul Mexican Grill",
  "logoUrl": "http://www.cielobluemexreservations.com/CieloBlueMexicanGrill_logo.jpg",
  "website": "http://www.cielobluecantina.com",
  "urls": [
    {
      "url": "http://www.ciellobluemexreservations.com",
      "laber": "Reservations"
    }
  ],
  "description": "We provide our customers with a fun and happy environment along with our enthusiastic staff, always making sure our customers have the greatest time in our restaurants. We try to make everyone of our customers feel welcome, and to make them have a great experience with us.",
  "email": "generalmgr@cielobluecantina.com",
  "openingHours": "Mo,Tu,We,Th,Fr 09:00-12:00",
  "hoursGeneralDescription": "Open 6 days a week, Tuesday to Sunday",
  "conditionsOfAccess": "reservations accepted",
  "locations": [
    {
      "streetAddress": "197 Bloor St E",
      "addressLocality": "Oshawa",
      "addressRegion": "ON",
      "postalCode": "L1H 3M3",
      "telephones": [
        "905-720-2326"
      ]
    }
  ],
  "categories": [
    "Food and Beverage"
  ],
  "subCategories": [
    "Mexican Food"
  ],
  "social": {
    "facebookUrl": "https://www.facebook.com/CieloBlueBelmont/",
    "instagramUrl": "https://www.instagram.com/CieloBlueBelmont/",
    "twitterUrl": "https://www.twitter.com/CieloBlueBelmont/",
    "youtubeUrl": "https://www.youtube.com/CieloBlueBelmont/",
    "yelpUrl": "https://www.yelp.com/biz/Cielo-Blue-Belmont"
  },
  "acceptedPaymentMethods": [
    "MasterCard",
    "Cash"
  ],
  "images": [
    "https://assets.ownlocal.com/images/a78feabb-df16-4fde-87aa-fba233d71671.jpeg",
    "https://assets.ownlocal.com/images/bbfe0e1f-0d8a-40df-86bd-c6a2250c09ec.jpeg"
  ]
}
```

This endpoint retrieves a specific business.

### HTTP Request

`GET https://admin.austin.ownlocal.com/api/v1/businesses/<uuid>`

### URL Parameters

Parameter | Description
--- | ---
uuid | The uuid of the business to retrieve

## Upload Image for a Business

```shell
curl -X POST "https://admin.austin.ownlocal.com/api/v1/businesses/<uuid>/images" \
 -H "Authorization: <token>" \
 -H "Content-Type: multipart/form-data" \
 -F "file=<file.png>;type=image/<format>" \
 -F "fileName=<file.png>
```

Use this endpoint to upload images for a specific business.

### URL Parameters

Parameter | Description
--- | ---
uuid | The business's uuid for which the image will be updloaded

### Form Parameters

Parameter | Type | Description
--- | --- | ---
file | image | The image to upload
name | string | The name that the file should be stored as. must include extension

## Upload Image for a Business

```shell
curl -X POST "https://admin.austin.ownlocal.com/api/v1/businesses/<uuid>/logo" \
 -H "Authorization: <token>" \
 -H "Content-Type: multipart/form-data" \
 -F "file=<file.png>;type=image/<format>" \
 -F "fileName=<file.png>
```

Use this endpoint to upload the logo for a specific business.

### URL Parameters

Parameter | Description
--- | ---
uuid | The business's uuid for which the logo will be updloaded

### Form Parameters

Parameter | Type | Description
--- | --- | ---
file | image | The image to upload
name | string | The name that the file should be stored as. must include extension
