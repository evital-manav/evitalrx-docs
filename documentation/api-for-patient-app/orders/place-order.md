---
description: To place order with items and its quantity.
---

# Place Order

## <img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Placing Orders with Ease: A Step-by-Step Guide](https://youtu.be/1TlUVPaWolI?si=2ybv22QYp_P3w994)

## Place Order

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/orders/place_order`](https://api.evitalrx.in/v1/patient/orders/place_order)

Here is the sample cURL request to place a pick-up online order with prescriptions. Use form data to call the place order API, and push prescriptions in the **image** param:

{% file src="../../.gitbook/assets/sample_curl - place_order.txt" %}

#### Request Body

| Name                                             | Type   | Description                                                                                                                                                                           |
| ------------------------------------------------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark>    | String | Id to uniquely identify the patient for whom the order is placed                                                                                                                      |
| items<mark style="color:red;">\*</mark>          | String | <p>Stringified Array of items with quantity (in pills) and medicine_id.</p><p><em>i.e.</em> [{"medicine_id":"Eli4pMFfzobV63G67jtjZw==","quantity": 10, "discount_percentage": 5}]</p> |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                                                                                                                                  |
| delivery\_type<mark style="color:red;">\*</mark> | String | Order Delivery type can be **pickup** or **delivery**                                                                                                                                 |
| address\_id<mark style="color:red;">\*</mark>    | String | Address ID from the address/list API.  required in case of the delivery\_type is "delivery"                                                                                           |
| parent\_patient\_id                              | String | If billing for family member, then pass parent patient's ID here.                                                                                                                     |
| order\_status                                    | String | It will save the order in the "draft" status.                                                                                                                                         |
| image                                            | File   | <p>Pass one or more prescription images in FormData.</p><p></p><p>allowed formats (png/jpg/jpeg)</p>                                                                                  |
| custom\_fields                                   | Object | <p>Key value pairs of attribute_key and it's value.<br>For ex: <br>{"prescription_id": "879", "appointment_id": "123"}</p>                                                            |
| shipping                                         | Number | <p>Shipping charge for delivery<br>(Will round up the given value<br>For ex: </p><p>20.5 => 21</p><p>20.2 => 20 )</p>                                                                 |
| remark                                           | String | Optional field to include any specific notes or instructions associated with the order.                                                                                               |



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

