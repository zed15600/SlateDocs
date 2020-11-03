# Categories

## Get Categories

```shell
curl "https://admin.austin.ownlocal.com/api/v1/categories" \
  -H "Authorization: <token>
```

> The above command returns JSON structured like this:

```json
[
  {
    "title": "Communication",
    "subCategories": [
      "Broadcasting Services",
      "Cable TV",
      "Newspapers and Magazines",
      "Other",
      "Publishing",
      "Radio Stations",
      "Telecommunications",
      "TV Stations"
    ]
  }
]
```

This endpoint return all categories

### HTTP Request

`GET https://admin.austin.ownlocal.com/api/v1/categories`

### Query Parameters

Parameter | Type | Default | Description
--- | --- | --- | ---
sortedBy | string | - | Specifies the sorting order
size | integer | 25 | Specifies the response size in businesses amount
page | integer | 1 | Specifies the page to retrieve based in the size parameter
