---
description: This API is used to accept the order.
---

# Mark as Accept

## Push the Order in Accepted state

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/orders/mark_as_accept`](https://api.evitalrx.in/v1/patient/orders/mark_as_accept)

This API marks the order in the accepted state.

#### Request Body

| Name                                        | Type   | Description                                     |
| ------------------------------------------- | ------ | ----------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token                            |
| order\_id<mark style="color:red;">\*</mark> | String | Order ID from the response of Place Order API.  |

{% tabs %}
{% tab title="200: OK Order accepted successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Order accepted successfully",
    "datetime": "2023-03-21 16:07:42",
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
