---
description: Get settings chemist has configured in eVitalRx for online orders.
---

# Get Chemist Order Settings

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/orders/get_chemist_order_settings`](https://api.evitalrx.in/v1/patient/orders/get_chemist_order_settings)

#### Request Body

| Name                                     | Type   | Description          |
| ---------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-02-08 12:15:13",
    "data": {
        "shipping_charges": "10", // pre-defined by chemist
        "minimum_order_value": "50" // // pre-defined by chemist
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "apikey is required",
    "datetime": "2024-02-08 12:16:17",
    "data": null
}
```
{% endtab %}
{% endtabs %}
