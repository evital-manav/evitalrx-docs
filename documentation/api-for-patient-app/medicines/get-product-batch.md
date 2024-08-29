---
description: To get item batches in your inventory by unique medicine Id.
---

# Get Product Batch



## Product Batches

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/search_medicine_by_batch`

Get Product Batches available in your inventory by Medicine Key.

#### Request Body

| Name                                           | Type   | Description                                                                                                            |
| ---------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication Token                                                                                                   |
| medicine\_id<mark style="color:red;">\*</mark> | String | Unique id of the Product                                                                                               |
| batch\_name                                    | String | <p>Batch Name of the Product. </p><p></p><p>If batch_name is provided, then only that batch information will come.</p> |

{% tabs %}
{% tab title="200: OK Batches Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-06-05 14:10:19",
    "data": [
        {
            "medicine_id": "buuFcMkpKTXqj7rxexDKew==",
            "id": "ApDrCEwcuRDrKJbu5dD5ww==",
            "batch": "BG015",
            "expiry": "2024-05-01",
            "mrp": 30.91,
            "price_to_retailer": 18,
            "quantity": 185,
            "cess_percentage": 0,
            "gst_percentage": 5,
            "margin": 10.75,
            "landing_price": 19.86,
            "expiry_label": "05/24",
            "margin_amount": 11.05,
            "margin_percentage": 35.75
        }
    ]
}
```
{% endtab %}

{% tab title="200: OK No Batches found" %}
```json
{
    "status_code": "0",
    "status_message": "No batches found for medicine",
    "datetime": "2022-12-07 11:23:46",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid medicine key",
    "datetime": "2022-12-07 11:24:25",
    "data": null
}
```
{% endtab %}
{% endtabs %}
