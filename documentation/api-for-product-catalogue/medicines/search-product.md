---
description: >-
  To search items in your inventory with the Item Name (string), GTIN number of
  the product, or Salt-Composition(content).
---

# Search Product

#### [Explore Medicines Available in Staging](../../getting-started-with-evitalrx.md#explore-medicines-available-in-staging)

## Search Products

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}catalog/medicines/search`](https://api.evitalrx.in/v1/catalog/medicines/search)

If the Item is present in your inventory, then it will appear first.

#### Request Body

| Name                                           | Type   | Description                                                                                                                                                                                                                                                                              |
| ---------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token                                                                                                                                                                                                                                                                     |
| searchstring<mark style="color:red;">\*</mark> | String | <p>Search String input</p><p>It can be used in following ways.</p><p>By Item Name</p><p><code>"searchstring":"dolo"</code></p><p></p><p>By Content</p><p><code>"searchstring":"c,paraceta"</code></p><p></p><p>By GTIN Number</p><p><code>"searchstring":"89080034169"</code></p><p></p> |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 15:16:32",
    "data": {
        "did_you_mean_result": [], // if medicine not found then suggestions
        "result": [
            {
                "dosage_type": "drop",
                "medicine_name": "Spasmex 20 mg/500 mg Drop",
                "content": "Dicyclomine (20mg) + Paracetamol (500mg)",
                "mrp": "22.5",
                "medicine_id": "5V9jvbzLGKcIwCOnnt5E/w==",
                "packing_size": "10 ml in 1 packet",
                "size": "1",
                "manufacturer_name": "Hema Laboratories",
                "medicine_type": "drug"
            },
            {
                "dosage_type": "drop",
                "medicine_name": "Lanol 100 Mg/ml Drop",
                "content": "Paracetamol (100mg/ml)",
                "mrp": "18",
                "medicine_id": "mvwaFPrEdzOHMTd9V9zsQg==",
                "packing_size": "1 Bottle of  15 Ml",
                "size": "1",
                "manufacturer_name": "Hetero Drugs Ltd",
                "medicine_type": "drug"
            }
        ]
    }    
}
```
{% endtab %}

{% tab title="200: OK Products not found" %}
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

{% tab title="200: OK Validation error" %}
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

**List of available medicines in the staging environment:**

{% file src="../../.gitbook/assets/staging_medicines.csv" %}



