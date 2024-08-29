---
description: To place order with items and its quantity.
---

# Place Order

## Place Order

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/orders/place_order`

Here is the sample cURL request to place a pick-up online order with prescriptions. Use form data to call the place order API, and push prescriptions in the **image** param.

more than 1 prescription is accepted. prescription can also be sent in the delivery orders. Copy & paste the below request in the postman, then any language code snippets can be generated with it.



curl --location 'https://api.evitalrx.in/v1/patient/orders/place\_order'\
\--form 'apikey="\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*"'\
\--form 'items="\[{"medicine\_id":"gv0GokYn9w4zFL51eouS2g==","quantity":50}]"'\
\--form 'patient\_id="yxu0Bh1hNM61K3b7t7+vlw=="'\
\--form 'delivery\_type="pickup"'\
\--form 'image=@"/C:/Users/91999/Downloads/image (51f8e0f5-d996-4d8e-91bb-752d923d88a6).png"'



#### Request Body

| Name                                             | Type   | Description                                                                                                                                                 |
| ------------------------------------------------ | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark>    | String | Id to uniquely identify the patient for whom the order is placed                                                                                            |
| items<mark style="color:red;">\*</mark>          | String | <p>Stringified Array of items with quantity (in pills) and medicine_id.</p><p><em>i.e.</em> [{"medicine_id":"Eli4pMFfzobV63G67jtjZw==","quantity": 10}]</p> |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                                                                                                        |
| delivery\_type<mark style="color:red;">\*</mark> | String | Order Delivery type can be **pickup** or **delivery**                                                                                                       |
| address<mark style="color:red;">\*</mark>        | String | Address of Patient for delivery                                                                                                                             |
| address\_line2                                   | String | Address Line 2 for long address                                                                                                                             |
| city<mark style="color:red;">\*</mark>           | String | City of Patient for delivery                                                                                                                                |
| state<mark style="color:red;">\*</mark>          | String | State of Patient for delivery                                                                                                                               |
| zipcode<mark style="color:red;">\*</mark>        | String | Zip code of Patient for delivery                                                                                                                            |
| parent\_patient\_id                              | String | If billing for family member, then pass parent patient's ID here.                                                                                           |
| order\_status                                    | String | It will save the order in the "draft" status.                                                                                                               |
| image                                            | File   | <p>Pass one or more prescription images in FormData.</p><p></p><p>allowed formats (png/jpg/jpeg)</p>                                                        |

{% tabs %}
{% tab title="200 Order Placed successfully." %}
```
{
    "status_code": "1",
    "status_message": "Order placed successfully",
    "datetime": "2022-12-06 18:46:31",
    "data": {
        "order_id": "/6vMKQj0JOB9GvN+6I27zg==",
        "order_number": "OJLBC8WC1I"
    }
}
```
{% endtab %}

{% tab title="200: OK Order failed." %}
```json
{
    "status_code": "0",
    "status_message": "Something went wrong",
    "datetime": "2022-12-06 18:47:41",
    "data": null
}
```
{% endtab %}
{% endtabs %}

