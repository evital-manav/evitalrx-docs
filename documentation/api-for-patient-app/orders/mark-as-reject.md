---
description: This API is used to reject the order.
---

# Mark as Reject

## Push the Order in Rejected state

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in//v1/patient/orders/mark_as_reject`

The orders in the "assigned", "accepted" and "shipped" states, can be canceled with this API.

#### Request Body

| Name                                             | Type   | Description                                                                 |
| ------------------------------------------------ | ------ | --------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                        |
| order\_id<mark style="color:red;">\*</mark>      | String | Order ID from the response of Place Order API.                              |
| reason\_source<mark style="color:red;">\*</mark> | String | <p>"pickup" | "delivery"</p><p></p><p>pass order is pickup or delivery.</p> |
| reason\_id<mark style="color:red;">\*</mark>     | Number | ID of the reasons got from Get Reject Reasons API.                          |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Your order cancelled successfully.",
    "datetime": "2023-03-21 16:05:47",
    "ng_version": "0.0.378",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "order_id is required",
    "datetime": "2023-03-09 17:03:38",
    "data": null
}
```
{% endtab %}
{% endtabs %}