---
description: >-
  To search items with the Item Name (string), GTIN number of the product, or
  Salt-Composition(content).
---

# Search

#### [Explore Medicines Available in Staging](../../getting-started-with-evitalrx.md#explore-medicines-available-in-staging)

## Search Products

<mark style="color:green;">`POST`</mark> [`https://staging-search.evitalrx.in/v1/fulfillment/medicines/pillo/search`](https://staging-search.evitalrx.in/v1/fulfillment/medicines/pillo/search)

#### Request Body

| Name                                           | Type   | Description                                                                                                                                                                                                                                                                       |
| ---------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| searchstring<mark style="color:red;">\*</mark> | String | <p>Search String input</p><p>It can be used in following ways.</p><p>By Item Name</p><p><code>"searchstring":"dolo"</code></p><p></p><p>By Content</p><p><code>"searchstring":"c,paraceta"</code></p><p></p><p>By GTIN Number</p><p><code>"searchstring":"89080034169"</code></p> |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token                                                                                                                                                                                                                                                              |

{% tabs %}
{% tab title="200 Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "SUCCESS",
    "datetime": "2025-09-09 11:48:20",
    "ng_version": "0.0.578",
    "data": {
        "search_type": "normal",
        "did_you_mean_result": [],
        "result": [
            {
                "accept_online_order": "yes",
                "discontinued": "no",
                "discount_percentage": 0,
                "gst_percentage": 12,
                "medicine_id": "X1P9/F3XVunOtftRNNCyHA==",
                "mrp": 30.74,
                "quantity": 0,
                "sell_in_loose": "yes",
                "available_for_patient": "yes",
                "content": "Paracetamol (650mg)",
                "dosage_type": "tablet",
                "gtin_number": "",
                "hsn_code": "30049061",
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/62d4e09cd4dd3.jpg",
                "is_rx_required": 0,
                "popularity_score": 72.72727272727273,
                "medicine_category": "drug",
                "primary_category_id": 819,
                "manufacturer_name": "Micro Labs Ltd",
                "medicine_name": "Dolo 650 Tablet",
                "medicine_name_suggest": "Dolo 650 Tablet",
                "medicine_type": "drug",
                "pack_size": "15 Tablet",
                "packing_size": "1 Strip of  15 Tablet",
                "price": 30.74,
                "salt_content_id": "+qIGHQHPc9AJh9QUPHyMSA==",
                "schedule_type": "H",
                "size": 15,
                "slug": "dolo-650-tablet-M00234T",
                "thumb_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/62d4e09cd4dd3.jpg",
                "watermark_free_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62d4e09cd4dd3.jpg",
                "price_per_unit": 2.05,
                "unit": "Tablet"
            },
            {
                "accept_online_order": "yes",
                "discontinued": "no",
                "discount_percentage": 0,
                "gst_percentage": 12,
                "medicine_id": "HD3nI9bnanVvGm6N6jthJw==",
                "mrp": 50,
                "quantity": 0,
                "sell_in_loose": "yes",
                "available_for_patient": "no",
                "content": "Losartan Potassium (100mg)",
                "dosage_type": "tablet",
                "gtin_number": "",
                "hsn_code": "0",
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/default.jpg",
                "is_rx_required": 0,
                "popularity_score": 46.96969696969697,
                "medicine_category": "",
                "primary_category_id": 0,
                "manufacturer_name": "Alkem Laboratories Ltd",
                "medicine_name": "Dolo 650 Tablet (15 Tablet)",
                "medicine_name_suggest": "Dolo 650 Tablet (15 Tablet)",
                "medicine_type": "",
                "pack_size": "15 Tablet",
                "packing_size": "1 Strip of  15 Tablet",
                "price": 50,
                "salt_content_id": "klejjWIyfAodC8J11IGD7w==",
                "schedule_type": "",
                "size": 15,
                "slug": "dolo-650-tablet-15-tablet-MDOTC316961964353",
                "thumb_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/default.jpg",
                "watermark_free_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                "price_per_unit": 3.33,
                "unit": "Tablet"
            },
            {
                "accept_online_order": "yes",
                "discontinued": "no",
                "discount_percentage": 0,
                "gst_percentage": 12,
                "medicine_id": "SfsO+h0OEdipWQ6ZZGwcZA==",
                "mrp": 0,
                "quantity": 0,
                "sell_in_loose": "yes",
                "available_for_patient": "no",
                "content": "Losartan Potassium (100mg)",
                "dosage_type": "tablet",
                "gtin_number": "",
                "hsn_code": "0",
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/default.jpg",
                "is_rx_required": 0,
                "popularity_score": 0,
                "medicine_category": "Drug",
                "primary_category_id": 0,
                "manufacturer_name": "Micro Labs Ltd",
                "medicine_name": "Dolo 650 Tablet (1 Tablet)",
                "medicine_name_suggest": "Dolo 650 Tablet (1 Tablet)",
                "medicine_type": "drug",
                "pack_size": "1 Tablet",
                "packing_size": "1 Strip of  1 Tablet",
                "price": 0,
                "salt_content_id": "klejjWIyfAodC8J11IGD7w==",
                "schedule_type": "",
                "size": 1,
                "slug": "dolo-650-tablet-1-tablet-MDDRG31541966617",
                "thumb_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/default.jpg",
                "watermark_free_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                "price_per_unit": 0,
                "unit": "Tablet"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK No Products found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 15:21:25",
    "data": {
        "did_you_mean_result": [],
        "result": []
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"Medicine Name\" length must be less than or equal to 20 characters long",
    "datetime": "2022-12-06 15:19:58",
    "data": null
}
```
{% endtab %}
{% endtabs %}

