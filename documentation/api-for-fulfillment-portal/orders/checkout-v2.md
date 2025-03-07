---
description: To check availability of the items.
---

# Checkout V2

## Get the availability of medicines

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/checkout_v2`](https://api.evitalrx.in/v1/fulfillment/orders/checkout_v2)

For the medicines which are out of stock, available alternative medicines will be provided.

#### Request Body

| Name                                          | Type    | Description                                                                                                                                                                                                                                                                                                                                                              |
| --------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark>      | String  | Authentication Token                                                                                                                                                                                                                                                                                                                                                     |
| patient\_id<mark style="color:red;">\*</mark> | String  | <p>Id to uniquely identify the patient for whom the order is placed  </p><p></p><p>if mobile is provided, then patient_id is optional.</p>                                                                                                                                                                                                                               |
| mobile                                        | String  | Patient's mobile no is optional if patient\_id is provided, required otherwise.                                                                                                                                                                                                                                                                                          |
| patient\_name                                 | String  | Patient's name is optional if patient\_id is provided, required otherwise.                                                                                                                                                                                                                                                                                               |
| items<mark style="color:red;">\*</mark>       | String  | <p>Stringified Array of Items.</p><p></p><p>Items should contain at least 1 object. </p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 20 (medicines)</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">"[{\"quantity\":1,\"medicine_id\":\"vVgL6Ggy5tYhqQr1qXOAzA==\"},{\"quantity\":2,\"medicine_id\":\"BXGcaezmfzcQEdh7fZVmUg==\"}]"
</code></pre> |
| latitude<mark style="color:red;">\*</mark>    | Number  | Latitude of the customer                                                                                                                                                                                                                                                                                                                                                 |
| longitude<mark style="color:red;">\*</mark>   | Number  | Longitude of the customer                                                                                                                                                                                                                                                                                                                                                |
| distance                                      | Number  | <p>Distance of fulfillment.<br><br>radius of search area for search provided item</p>                                                                                                                                                                                                                                                                                    |
| find\_alternative                             | Boolean | Flag to get item alternatives                                                                                                                                                                                                                                                                                                                                            |



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-03-07 12:37:40",
    "version": "1.1.46",
    "data": {
        "shipping_charges": 30,
        "chemist_details_list": [
            {
                "chemist_id": "EQYmBF/sPyAcIbTXvZ6vRA==",
                "distance": "0",
                "chemist_details": {
                    "pharmacy_name": "Demo Pharmacy",
                    "pharmacy_logo": "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/col6p1dhuv.jpg",
                    "store_photos": [
                        "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/35kddetdv0.png"
                    ],
                    "full_address": "Evital Rx 4d Square Mall, Ahmedabad, Gujarat, India, 380005",
                    "latitude": "23.1025849",
                    "longitude": "72.5953601"
                }
            }
        ],
        "items": [
            {
                "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                "mrp": 42.83,
                "price": 38.55,
                "discount_percentage": 10,
                "available": "yes",
                "alternatives": []
            },
            {
                "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                "mrp": 23.5,
                "price": 21.15,
                "discount_percentage": 10,
                "available": "yes",
                "alternatives": []
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Invalid params" %}
```json
{
    "status_code": "0",
    "status_message": "longitude is required",
    "datetime": "2023-02-15 12:46:54",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK No pharmacy found" %}
```json
{
    "status_code": "0",
    "status_message": "No Pharmacies found near by your location",
    "datetime": "2023-02-15 12:37:11",
    "data": null
}
```
{% endtab %}
{% endtabs %}
