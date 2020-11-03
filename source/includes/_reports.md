# Reports

## Ads

```shell
curl "https://admin.austin.ownlocal.com/api/v1/reports/ads" \
  -H "Authorization: <token>
```

> The above command returns JSON structured like this:

```json
{
  "start_date": "2020-06-01",
  "end_date": "2020-07-01",
  "publisher_name": "The Pub News",
  "publisher_id": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "ads": [
    {
      "uuid": "87415afa-ac85-4f55-b869-c63532d02ffe",
      "start_date": "2020-06-24",
      "end_date": "2020-06-25",
      "data": {
        "online_impressions": {
          "overall": 11346
        },
        "interaction_breakdown": {
          "breakdowns": {
            "overall": {
              "total_clicks": 9,
              "about_us_clicks": 0,
              "contact_clicks": 0,
              "expand_ad_unit_clicks": 9,
              "print_ad_clicks": 0,
              "website_clicks": 0,
              "facebook_clicks": 0,
              "twitter_clicks": 0,
              "instagram_clicks": 0,
              "yelp_clicks": 0,
              "call_clicks": 0,
              "directions_clicks": 0,
              "contact_form_submits": 0,
              "share": 0
            }
          }
        }
      }
    },
    {
      "uuid": "a3c6f485-07b1-4241-9bc7-9945be77d0a5",
      "data": {
        "online_impressions": {
          "overall": 11410
        },
        "interaction_breakdown": {
          "breakdowns": {
            "overall": {
              "total_clicks": 4,
              "about_us_clicks": 0,
              "contact_clicks": 0,
              "expand_ad_unit_clicks": 4,
              "print_ad_clicks": 0,
              "website_clicks": 0,
              "facebook_clicks": 0,
              "twitter_clicks": 0,
              "instagram_clicks": 0,
              "yelp_clicks": 0,
              "call_clicks": 0,
              "directions_clicks": 0,
              "contact_form_submits": 0,
              "share": 0
            }
          }
        }
      }
    }
  ]
}
```

This endpoint returns reports data for all the ads running during the given dates.

### HHTP Request

`GET https://admin.austin.ownlocal.com/api/v1/reports/ads`

### Query Parameters

Parameter | Type | Default | Description
--- | --- | --- | ---
publisher_id | string | - | Returns reports only for ads published by the provided partner
start_date | date | 1 month ago | Sets the start date for the report's data
end_date | date | today | Sets the end date for the report's data

## Business

```shell
curl "https://admin.austin.ownlocal.com/api/v1/reports/business" \
  -H "Authorization: <token>
```

> The above command returns JSON structured like this:

```json
{
  "start_date": "2020-06-01",
  "end_date": "2020-07-01",
  "business_name": "My Local Business",
  "business_id": "2db5e240-c098-4d59-b3a3-bc7b7abc2c4c",
  "reach_report": {
    "print_distribution": 0,
    "online_impressions": {
      "overall": 277160
    },
    "total_ads": 13,
    "directory": {
      "days": 31,
      "impressions": 0
    },
    "origami": {
      "ads": 9,
      "days": 10,
      "impressions": {
        "overall": 277160
      }
    },
    "interaction_breakdown": {
      "breakdowns": {
        "overall": {
          "total_clicks": 209,
          "about_us_clicks": 1,
          "contact_clicks": 0,
          "expand_ad_unit_clicks": 181,
          "print_ad_clicks": 0,
          "website_clicks": 19,
          "facebook_clicks": 0,
          "twitter_clicks": 0,
          "instagram_clicks": 0,
          "yelp_clicks": 0,
          "call_clicks": 1,
          "directions_clicks": 7,
          "contact_form_submits": 0,
          "share": 0
        }
      }
    }
  }
}
```

This endpoint returns reports data for a specific business in the given dates.

### HTTP Request

`GET https://admin.austin.ownlocal.com/api/v1/reports/business`

### Query Parameters
Parameter | Type | Default | Description
--- | --- | --- | ---
publisher_id | string | - | Required. The partner the business is listed under.
business_id | string | - | The business to generate data from. If not provided, all partner's businesses reports will be generated
start_date | date | 1 month ago | Sets the start date for the report's data
end_date | date | today | Sets the end date for the report's data
