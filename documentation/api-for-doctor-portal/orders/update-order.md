---
description: This API is deprecated.
---

# ⛔ Update Order

## Update order

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}doctor/orders/update_order`](https://api.evitalrx.in/v1/doctor/orders/update_order)

#### Request Body

| Name                                        | Type   | Description                                                                                                                                                             |
| ------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| order\_id<mark style="color:red;">\*</mark> | String | Unique id of the order                                                                                                                                                  |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token                                                                                                                                                    |
| items                                       | String | <p>Stringified Array of Items.</p><p></p><p>i.e.</p><p>[{"medicine_id":"ZnsQl586DmR/ANT3aLdM4g==","batch_id":"lhk/Qty04EUD42YJqOgYhA==","discount":0,"quantity":3}]</p> |

{% tabs %}
{% tab title="200: OK Order updated successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Order updated successfully",
    "datetime": "2022-12-08 18:32:25",
    "data": {
        "amount": "345", // updated amount
        "order_number": "OGLBF2YAYW",
        "order_id": "Kv1Dmatn3q7QW147CsWKAg=="
    }
}
```
{% endtab %}

{% tab title="200: OK Could not find an order matching this query." %}
```json
{
    "status_code": "0",
    "status_message": "No record found",
    "datetime": "2022-12-07 14:30:56",
    "data": null
}
```
{% endtab %}
{% endtabs %}
