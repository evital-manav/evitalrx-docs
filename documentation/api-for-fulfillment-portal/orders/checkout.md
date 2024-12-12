---
description: To check availability of the items.
---

# Checkout

## Get the availability of medicines

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/checkout`](https://api.evitalrx.in/v1/fulfillment/orders/checkout)

For the medicines which are out of stock, available alternative medicines will be provided.

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                                                                                                                                                                                              |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark> | String | Authentication Token                                                                                                                                                                                                                                                                                                                                                     |
| items<mark style="color:red;">\*</mark>  | String | <p>Stringified Array of Items.</p><p></p><p>Items should contain at least 1 object. </p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 20 (medicines)</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">"[{\"quantity\":1,\"medicine_id\":\"vVgL6Ggy5tYhqQr1qXOAzA==\"},{\"quantity\":2,\"medicine_id\":\"BXGcaezmfzcQEdh7fZVmUg==\"}]"
</code></pre> |
| latitude                                 | Number | Latitude of the customer                                                                                                                                                                                                                                                                                                                                                 |
| longitude                                | Number | Longitude of the customer                                                                                                                                                                                                                                                                                                                                                |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-09-18 11:52:03",
    "data": {
        "shipping_charges": 124,
        "items": [
            {
                "medicine_id": "BXGcaezmfzcQEdh7fZVmUg==",
                "mrp": 36.1,
                "price": 36.1,
                "available": "yes",
                "alternatives": [] // alternatives, if any
            },
            {
                "medicine_id": "vVgL6Ggy5tYhqQr1qXOAzA==",
                "mrp": 41.8,
                "price": 41.8,
                "available": "no",
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
