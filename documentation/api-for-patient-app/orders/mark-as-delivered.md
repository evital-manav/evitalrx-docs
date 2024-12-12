---
description: This API is used to complete your order.
---

# Mark as Delivered

## Push the Order in delivered state

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/orders/mark_as_delivered`](https://api.evitalrx.in/v1/patient/orders/mark_as_delivered)

This API marks the order in the delivered state. This API will complete the order.

#### Request Body

| Name                                              | Type   | Description                                                                                                                                                    |
| ------------------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>          | String | Authentication token                                                                                                                                           |
| delivery\_pin                                     | String | Required for pickup orders. Not required for the delivery orders.                                                                                              |
| order\_id<mark style="color:red;">\*</mark>       | String | Order ID from the response of Place Order API.                                                                                                                 |
| payment\_status<mark style="color:red;">\*</mark> | Number | <p>To choose payment mode of the order. </p><p>1: CASH </p><p>2: CREDIT </p><p>3: UPI </p><p>4: CHEQUE </p><p>5: PAYTM </p><p>6: CC/DC </p><p>7: RTGS/NEFT</p> |

{% tabs %}
{% tab title="200: OK Order delivered successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Order Delivered successfully",
    "datetime": "2023-03-09 14:39:53",
    "ng_version": "0.0.371",
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
