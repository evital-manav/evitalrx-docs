---
description: >-
  To search items with the Item Name (string), GTIN number of the product, or
  Salt-Composition(content).
---

# Search Products

#### [Explore Medicines Available in Staging](../../getting-started-with-evitalrx.md#explore-medicines-available-in-staging)

## Search Products

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}fulfillment/medicines/search`](https://api.evitalrx.in/v1/fulfillment/medicines/search)

If the Item is present in your inventory, then it will appear first.

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
    "status_message": "Success",
    "datetime": "2022-12-06 17:49:55",
    "data": {
        "did_you_mean_result": [], // if medicine not found then suggestions
        "result": [
            {
                "dosage_type": "",
                "medicine_name": "LTK-H Tablet 5",
                "content": "",
                "mrp": 24,
                "price": "32.9",
                "medicine_id": "otUfMtG4nIpWSc+oWoX7Lw==",
                "packing_size": "1 Strip of  15 Tablet",
                "size": "15",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "medicine_type": "otc",
                "gst_percentage": "12",
                "available_for_patient": "yes",
                "discontinued": "no",
                "loose_quantity": 1305,
                "sale_discount": 0,
                "strip_quantity": 87,
                "is_inventory_available": "yes",
                "sell_in_loose": "yes"
            },
            {
                "dosage_type": "",
                "medicine_name": "Ltk 50 Tablet",
                "content": "Losartan (50mg)",
                "mrp": 115,
                "price": "23.5",
                "medicine_id": "ZnsQl586DmR/ANT3aLdM4g==",
                "packing_size": "10 tablets in 1 strip",
                "size": "10",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "medicine_type": "drug",
                "gst_percentage": "5",
                "available_for_patient": "yes",
                "discontinued": "no",
                "loose_quantity": 100,
                "sale_discount": 0,
                "strip_quantity": 10,
                "is_inventory_available": "yes",
                "sell_in_loose": "yes"
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

