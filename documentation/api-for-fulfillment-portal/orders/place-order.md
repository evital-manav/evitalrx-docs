---
description: To place order with items and its quantity.
---

# Place Order

## Place Order

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/fulfillment/orders/place_order`

&#x20;

#### Request Body

| Name                                             | Type   | Description                                                                                                                                                                                                                                       |
| ------------------------------------------------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark>    | String | <p>Id to uniquely identify the patient for whom the order is placed  </p><p></p><p>if mobile is provided, then patient_id is optional.</p>                                                                                                        |
| items<mark style="color:red;">\*</mark>          | String | <p>Stringified Array of items with quantity (in strip) and medicine_id.</p><p><em>i.e.</em> [{"medicine_id":"Eli4pMFfzobV63G67jtjZw==","quantity": 2}]</p><p></p>                                                                                 |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                                                                                                                                                                                              |
| delivery\_type<mark style="color:red;">\*</mark> | String | Order Delivery type can be **pickup** or **delivery**                                                                                                                                                                                             |
| address<mark style="color:red;">\*</mark>        | String | Address of Patient for delivery. required if delivery\_type is **delivery**                                                                                                                                                                       |
| address\_line2                                   | String | Address Line 2 for long address                                                                                                                                                                                                                   |
| city<mark style="color:red;">\*</mark>           | String | City of Patient for delivery                                                                                                                                                                                                                      |
| state<mark style="color:red;">\*</mark>          | String | State of Patient for delivery                                                                                                                                                                                                                     |
| zipcode<mark style="color:red;">\*</mark>        | String | Zip code of Patient for delivery                                                                                                                                                                                                                  |
| mobile                                           | String | Patient's mobile no is optional if patient\_id is provided, required otherwise.                                                                                                                                                                   |
| patient\_name                                    | String | Patient's name is optional if patient\_id is provided, required otherwise.                                                                                                                                                                        |
| latitude                                         | Number | Latitude of the patient to search in nearby pharmacies.                                                                                                                                                                                           |
| longitude                                        | Number | Longitude of the patient to search in the nearby pharmacies.                                                                                                                                                                                      |
| full\_address                                    | String | <p>Required If lat-long is not provided. This address is used to get the lat-long to find the nearest pharmacy store.</p><p></p><p>Only zipcode can also by passed in this param </p><p></p><p>like <code>{ "full_address": "560008" }</code></p> |

{% tabs %}
{% tab title="200 Order Placed successfully." %}
```
{
    "status_code": "1",
    "status_message": "Order placed successfully",
    "datetime": "2023-02-14 19:23:51",
    "data": {
        "order_id": "FjauqxGgQYVpkl57jXYMhg==",
        "order_number": "OQLE4B1Z8F",
        "total": 111,
        "thankyou_msg_first": "Thank You",
        "thankyou_msg_second": "Your order has been placed to ",
        "pharmacy_name": "API medicals"
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

