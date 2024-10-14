---
description: Get list of reasons to reject the order.
---

# Get Reject Reasons

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/fulfillment/orders/reject_reasons`

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
    "datetime": "2023-03-21 17:18:14",
    "data": {
        "reasons": [
            {
                "id": 1,
                "reason": "Medicine not available"
            },
            {
                "id": 2,
                "reason": "Can't deliver in this area"
            },
            {
                "id": 4,
                "reason": "Delivery person not available"
            },
            {
                "id": 5,
                "reason": "Less order value"
            },
            {
                "id": 6,
                "reason": "Store closed"
            },
            {
                "id": 21,
                "reason": "Prescription not attached in this order"
            },
            {
                "id": 10,
                "reason": "Can't modify MRP"
            },
            {
                "id": 7,
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
