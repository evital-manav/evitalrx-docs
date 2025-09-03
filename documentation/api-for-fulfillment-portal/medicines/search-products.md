---
description: >-
  To search items with the Item Name (string), GTIN number of the product, or
  Salt-Composition(content).
---

# Search

#### [Explore Medicines Available in Staging](../../getting-started-with-evitalrx.md#explore-medicines-available-in-staging)

## Search Products

<mark style="color:green;">`POST`</mark> [`https://search.evitalrx.in/v1/fulfillment/medicines/pillo/search`](https://search.evitalrx.in/v1/fulfillment/medicines/pillo/search)&#x20;

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
    "datetime": "2025-07-01 15:02:32",
    "ng_version": "0.0.578",
    "data": {
        "search_type": "normal",
        "did_you_mean_result": [],
        "result": [
            {
                "accept_online_order": "yes",
                "cess_percentage": 0,
                "chemist_id": 0,
                "directions": "0-0-0-0",
                "discontinued": "no",
                "discount_percentage": 0,
                "gst_percentage": 12,
                "inventory_id": 0,
                "item_category": "",
                "item_category_id": 0,
                "item_lock": "no",
                "location": "",
                "lock_b2b_discount": "no",
                "lock_discount": "no",
                "max_quantity": 0,
                "medicine_id": "buuFcMkpKTXqj7rxexDKew==",
                "medicine_short_tag": "",
                "min_quantity": 0,
                "mrp": 33.76,
                "onboarding_medicine_name": "",
                "quantity": 0,
                "sale_b2b_discount": 0,
                "sale_count": 0,
                "sale_discount": 0,
                "sell_in_loose": "yes",
                "batch": "",
                "batch_discount": 0,
                "expiry": "",
                "landing_price": 0,
                "price_to_retailer": 0,
                "skucode": "",
                "approved": 0,
                "available_for_patient": "yes",
                "content": "Paracetamol (650mg)",
                "dosage_type": "tablet",
                "gtin_number": "",
                "hsn_code": "30049061",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/676fcd36f12eb.jpg",
                "is_rx_required": 1,
                "popularity_score": 100,
                "manufacturer_name": "Micro Labs Ltd",
                "medicine_name": "Dolo 650 Tablet",
                "medicine_name_suggest": "Dolo 650 Tablet",
                "medicine_type": "drug",
                "pack_size": "15 Tablet",
                "packing_size": "1 Strip of  15 Tablet",
                "price": 33.76,
                "salt_content_id": "wnSfhg0Ybp7Nlo2mOVkoNQ==",
                "schedule_type": "H",
                "size": 15,
                "slug": "dolo-650-tablet-15-tablet-M00234T",
                "thumb_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/thumb/676fcd36f12eb.jpg",
                "watermark_free_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/itemoriginalcopy/medicines/676fcd36f12eb.jpg",
                "requested_by_entity": "chemist"
            },
            {
                "accept_online_order": "yes",
                "cess_percentage": 0,
                "chemist_id": 0,
                "directions": "0-0-0-0",
                "discontinued": "no",
                "discount_percentage": 0,
                "gst_percentage": 12,
                "inventory_id": 0,
                "item_category": "",
                "item_category_id": 0,
                "item_lock": "no",
                "location": "",
                "lock_b2b_discount": "no",
                "lock_discount": "no",
                "max_quantity": 0,
                "medicine_id": "niQUCJ+B1q7/JCUN9pqzsA==",
                "medicine_short_tag": "",
                "min_quantity": 0,
                "mrp": 33.6,
                "onboarding_medicine_name": "",
                "quantity": 0,
                "sale_b2b_discount": 0,
                "sale_count": 0,
                "sale_discount": 0,
                "sell_in_loose": "yes",
                "batch": "",
                "batch_discount": 0,
                "expiry": "",
                "landing_price": 0,
                "price_to_retailer": 0,
                "skucode": "",
                "approved": 0,
                "available_for_patient": "yes",
                "content": "Paracetamol (650mg)",
                "dosage_type": "tablet",
                "gtin_number": "",
                "hsn_code": "30049099",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/50ef1e84-2740-11f0-8097-0242ac140002.jpg",
                "is_rx_required": 1,
                "popularity_score": 99.2773,
                "manufacturer_name": "Micro Labs Ltd",
                "medicine_name": "Dolo 650 Tablet",
                "medicine_name_suggest": "Dolo 650 Tablet",
                "medicine_type": "drug",
                "pack_size": "10 Tablet",
                "packing_size": "1 Strip of  10 Tablet",
                "price": 33.6,
                "salt_content_id": "wnSfhg0Ybp7Nlo2mOVkoNQ==",
                "schedule_type": "H",
                "size": 10,
                "slug": "dolo-650-tablet-M00LVL2",
                "thumb_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/thumb/50ef1e84-2740-11f0-8097-0242ac140002.jpg",
                "watermark_free_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/itemoriginalcopy/medicines/50ef1e84-2740-11f0-8097-0242ac140002.jpg",
                "requested_by_entity": "chemist",
                "updated_ip": "::1",
                "updated_date": "2025-06-26 01:02:44"
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

