---
description: To place order with items and its quantity.
---

# Place Order V3

Place Order API has two flow:

1. **Manual Flow** : The available items are passed and order can be placed.
2. **Prescription Digitization Flow** : In this flow only prescription will be provided which will be digitized at our end then, order will be placed.

> In API request, You need to pass either provide **patient\_id** or **mobile & patient\_name**.

## <img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Placing Orders with Ease: A Step-by-Step Guide](https://youtu.be/1TlUVPaWolI?si=2ybv22QYp_P3w994)

## Place Order

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/place_order_v3`](https://dev-api.evitalrx.in/v1/fulfillment/orders/place_order_v3)

#### Request Body

| Name                                              | Type   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>          | String | Authentication token                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| location\_token<mark style="color:red;">\*</mark> | String | Get token from Check Serviceability V3 API                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| patient\_id<mark style="color:red;">\*</mark>     | String | <p>Id to uniquely identify the patient for whom the order is placed  </p><p></p><p>if mobile and patient name is provided, then patient_id is optional.</p>                                                                                                                                                                                                                                                                                                                                                                           |
| items<mark style="color:red;">\*</mark>           | String | <p>Stringified Array of items with quantity (in strip) and medicine_id.</p><p><em>i.e.</em> [{"medicine_id":"Eli4pMFfzobV63G67jtjZw==","quantity": 2}]</p><p><br>Provide only available items which can be know from checkout V3.</p><p><br>Pass "discount_percentage" along with "medicine_id" and quantity to apply custom discount on the item.</p>                                                                                                                                                                                |
| delivery\_type<mark style="color:red;">\*</mark>  | String | Order Delivery type can be **pickup** or **delivery**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| address<mark style="color:red;">\*</mark>         | String | Address of Patient for delivery. required if delivery\_type is **delivery**                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| address\_line2                                    | String | Address Line 2 for long address                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| city<mark style="color:red;">\*</mark>            | String | City of Patient for delivery                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| state<mark style="color:red;">\*</mark>           | String | State of Patient for delivery                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| zipcode<mark style="color:red;">\*</mark>         | String | Zip code of Patient for delivery                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| latitude                                          | Number | Latitude of the patient to search in nearby pharmacies.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| longitude                                         | Number | Longitude of the patient to search in the nearby pharmacies.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| mobile                                            | String | Patient's mobile no is optional if patient\_id is provided, required otherwise.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| patient\_name                                     | String | Patient's name is optional if patient\_id is provided, required otherwise.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| prescription\_urls                                | String | <p>Stringified Array of prescription URLs.​</p><p></p><p><strong>items</strong> param is optional, if <strong>prescription_urls</strong> param is passed.​</p><p></p><p><strong>prescription_urls</strong> is mandatory for RX medicine.(Check is_rx_required from <a href="checkout-v3.md">checkout</a>)</p><p></p><p>For eg.</p><p>["https://www.klippa.com/wp-content/uploads/2020/12/medical-prescription-ocr.png","https://as2.ftcdn.net/v2/jpg/00/56/61/71/500_F_56617167_ZGbrr3mHPUmLoksQmpuY7SPA8ihTI5Dh.jpg"]</p><p><br></p> |
| full\_address                                     | String | <p>Required If lat-long is not provided. This address is used to get the lat-long to find the nearest pharmacy store.</p><p></p><p>Only zipcode can also by passed in this param </p><p></p><p>like <code>{ "full_address": "560008" }</code></p>                                                                                                                                                                                                                                                                                     |
| requestId                                         | String | Partner order id                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

{% tabs %}
{% tab title="200 Order Placed successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Order placed successfully",
    "datetime": "2025-03-13 17:52:30",
    "version": "1.1.51",
    "data": {
        "order_id": "F7VH/hoYLmOIBrCiHyccng==",
        "order_number": "OOM87BK5Y7",
        "total_amount": 119,
        "total": 149,
        "split_orders": [
            {
                "order_id": "7xS09/uGsj9fglWVxIw97Q==",
                "order_number": "O2M87BK68H",
                "chemist_details": {
                    "chemist_id": "GJmQXzl+VAVkke3efyTrcw==",
                    "pharmacy_name": "Demo Pharmacy",
                    "full_address": "Evital Rx 4d Square Mall, Ahmedabad, Gujarat, India, 380005",
                    "latitude": "23.1025849",
                    "longitude": "72.5953601",
                    "zipcode": "380005"
                }
            }
        ]
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

