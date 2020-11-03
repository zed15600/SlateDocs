# Models

## Ad

```json
{
  "adUuid(string)":	"795d064b-1810-4f6b-bada-6a9f7d534579",
  "fileName(string)": "{original_filename}.pdf",
  "adCustomId(string)": "234567",
  "businessUuid(string)": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "publisherUuid(string)": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "image(string)": "https://assets.ownlocal.com/ads/795d064b-1810-4f6b-bada-6a9f7d534579/order_image.jpeg",
  "startDate(date)": "2019-09-01",
  "endDate(date)": "2019-09-30",
  "dateModified(date)": "2019-09-03",
  "dateCreated(date)": "2019-09-03",
  "adText(string)": "This is an example ad text.",
  "offerCount(integer)": 4,
  "offers(array)": [{...}]
}
```

## Offer

```json
{
  "offerUuid(string)": "bbfdc747-b2c9-4232-be7a-81dbf5290af4",
  "offerImage(string)": "https://ownlocal.imgix.net/offers/bbfdc747-b2c9-4232-be7a-81dbf5290af4.png",
  "title(string)": "40% Off Full Interior Detail Package",
  "description(string)": "This is an example text",
  "originalPrice(string)": "This is an example text",
  "discountPercentage(string)": "40",
  "discountPrice(string)": "This is an example text",
  "discountOff(string)": "This is an example text",
  "newPrice(string)": "This is an example text",
  "bogo(boolean)": false,
  "free(boolean)": false,
  "validThrough(string)": "This is an example text",
  "gtin8(array)":	[
    {
      "class(integer)": 77011700
    },
    {...}
  ]
}
```

## Business

```json
{
  "businessUuid(string)": "69271d95-e891-4bf7-a9ba-ce249e36e236",
  "businessCustomId(string)": "23456",
  "publisherUuids(array)":	[
    "e94df8d7-cc45-4ec9-b9fa-e42f04f74c38",
    "9103093d-596a-4ed4-a0ea-d7a5bfc35912"
  ],
  "name(string)": "Cielo Azul Mexican Grill",
  "logoUrl(string)": "http://www.cielobluemexreservations.com/CieloBlueMexicanGrill_logo.jpg",
  "website(string)": "http://www.cielobluecantina.com",
  "urls(array)": [
    {
      "url(string)": "www.exampleurl.com",
      "label(string)": "homepage"
    },
    {...}
  ],
  "description(string)": "We provide our customers with a fun and happy environment along with our enthusiastic staff, always making sure our customers have the greatest time in our restaurants. We try to make everyone of our customers feel welcome, and to make them have a great experience with us.",
  "email(string)": "generalmgr@cielobluecantina.com",
  "openingHours(string)": "Mo,Tu,We,Th,Fr 09:00-12:00",
  "hoursGeneralDescription(string)": "Open 6 days a week, Tuesday to Sunday",
  "conditionsOfAccess(string)": "reservations accepted",
  "locations(array)":	[
    {
      "streetAddress(string)": "197 Bloor St E",
      "addressLocality(string)": "Oshawa",
      "addressRegion(string)": "ON",
      "postalCode(string)": "L1H 3M3",
      "telephones(array)": [
        "905-720-2326",
        "905-720-2326",
      ]
    },
    {...}
  ],
  "categories(array)": [
    "Food and Beverage"
  ],
  "subCategories(array)": [
    "Mexican Food"
  ],
  "social(object)": {
    "facebookUrl(string)": "https://www.facebook.com/CieloBlueBelmont/",
    "instagramUrl(string)": "https://www.instagram.com/CieloBlueBelmont/",
    "twitterUrl(string)": "https://www.twitter.com/CieloBlueBelmont/",
    "youtubeUrl(string)": "https://www.youtube.com/CieloBlueBelmont/",
    "yelpUrl(string)": "https://www.yelp.com/biz/Cielo-Blue-Belmont"
  },
  "acceptedPaymentMethods(array)": [
    "MasterCard",
    "Cash"
  ],
  "images(array)": [
    "https://assets.ownlocal.com/images/a78feabb-df16-4fde-87aa-fba233d71671.jpeg",
    "https://assets.ownlocal.com/images/bbfe0e1f-0d8a-40df-86bd-c6a2250c09ec.jpeg"
  ]
}
```
