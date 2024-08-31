---
description: >-
  To search items with the Item Name (string), GTIN number of the product, or
  Salt-Composition(content).
---

# Search Products

## Search Products

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/search`

If the Item is present in your inventory, then it will appear first.

#### Request Body

| Name                                           | Type   | Description                                                                                                                                                                                                                                                                       |
| ---------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| searchstring<mark style="color:red;">\*</mark> | String | <p>Search String input</p><p>It can be used in following ways.</p><p>By Item Name</p><p><code>"searchstring":"dolo"</code></p><p></p><p>By Content</p><p><code>"searchstring":"c,paraceta"</code></p><p></p><p>By GTIN Number</p><p><code>"searchstring":"89080034169"</code></p> |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token                                                                                                                                                                                                                                                              |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-07 10:49:06",
    "data": {
        "did_you_mean_result": [],
        "result": [
            {
                "dosage_type": "tablet",
                "medicine_name": "Cold N Flu Tablet",
                "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
                "mrp": 78,
                "medicine_id": "8HiQkGfpzbiAzkma2b5/yw==",
                "packing_size": "1 Strip of  10 Tablet",
                "size": "10",
                "manufacturer_name": "Elder Labs Limited",
                "medicine_type": "drug",
                "gst_percentage": "12",
                "available_for_patient": "yes",
                "discontinued": "no",
                "loose_quantity": 4970,
                "sale_discount": 0,
                "strip_quantity": 497,
                "is_inventory_available": "yes",
                "sell_in_loose": "yes"
            },
            {
                "dosage_type": "tablet",
                "medicine_name": "N-Cold New Tablet",
                "content": "Paracetamol (325mg) + Phenylephrine (2.5mg) + Chlorpheniramine (2mg)",
                "mrp": 48.6,
                "medicine_id": "RYmIov0OJ2TM7qQEJ2YRqw==",
                "packing_size": "1 Strip of  10 Tablet",
                "size": "10",
                "manufacturer_name": "German Remedies Pharmaceuticals Pvt Ltd",
                "medicine_type": "drug",
                "gst_percentage": "12",
                "salt_content_id": "18885",
                "available_for_patient": "yes",
                "discontinued": "no",
                "loose_quantity": 3970,
                "sale_discount": 0,
                "strip_quantity": 397,
                "is_inventory_available": "yes",
                "sell_in_loose": "yes"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK No Product found according to search query" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-07 10:50:10",
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

**List of Medicines available in the staging environment:**

{% file src="../../.gitbook/assets/staging_medicines.csv" %}