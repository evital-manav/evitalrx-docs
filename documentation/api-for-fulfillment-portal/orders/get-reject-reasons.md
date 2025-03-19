---
description: Get list of reasons to reject the order.
---

# Get Reject Reasons

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/reject_reasons`](https://api.evitalrx.in/v1/fulfillment/orders/reject_reasons)

#### Request Body

| Name                                             | Type   | Description                                                                 |
| ------------------------------------------------ | ------ | --------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                        |
| reason\_source<mark style="color:red;">\*</mark> | String | <p>"pickup" | "delivery"</p><p></p><p>pass order is pickup or delivery.</p> |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-03-19 11:13:52",
    "version": "1.1.64",
    "data": {
        "reasons": [
            {
                "id": 50,
                "reason": "Wrong medicines order"
            },
            {
                "id": 51,
                "reason": "Order placed on wrong address"
            },
            {
                "id": 52,
                "reason": "No response in order"
            },
            {
                "id": 49,
                "reason": "Discount is less"
            },
            {
                "id": 53,
                "reason": "By mistake place an order"
            },
            {
                "id": 61,
                "reason": "Other"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "reason_source must be one of [pickup, delivery]",
    "datetime": "2023-03-21 17:19:21",
    "data": null
}
```
{% endtab %}
{% endtabs %}
