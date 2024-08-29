---
description: To get item batches in your inventory by unique medicine Id.
---

# Get Product Batch



## Product Batches

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/get_batches`

Get Product Batches available in your inventory by Medicine Key.

#### Request Body

| Name                                           | Type   | Description              |
| ---------------------------------------------- | ------ | ------------------------ |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication Token     |
| medicine\_id<mark style="color:red;">\*</mark> | String | Unique id of the product |

{% tabs %}
{% tab title="200: OK Batches Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-08 15:11:10",
    "data": [
        {
            "medicine_id": "otUfMtG4nIpWSc+oWoX7Lw==",
            "id": "o5+9ckBfrNDerV+gyQmOCQ==",
            "batch": "ABC",
            "expiry": "2025-12-01",
            "mrp": 24,
            "price_to_retailer": 15,
            "quantity": 1230,
            "expiry_label": "12/25"
        },
        {
            "medicine_id": "otUfMtG4nIpWSc+oWoX7Lw==",
            "id": "/GuD64lAIn9WMiGQGFUuaA==",
            "batch": "PQR",
            "expiry": "2026-12-01",
            "mrp": 24,
            "price_to_retailer": 15,
            "quantity": 150,
            "expiry_label": "12/26"
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
