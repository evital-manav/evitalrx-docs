---
description: To check availability of the items.
---

# Checkout

## Get availability of medicines

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/fulfillment/orders/checkout`

For the medicines which are out of stock, available alternative medicines will be provided.

#### Request Body

| Name                                            | Type   | Description                                                                                                                                                                                                                                              |
| ----------------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>        | String | Authentication Token                                                                                                                                                                                                                                     |
| medicine\_ids<mark style="color:red;">\*</mark> | String | <p>Stringified Array of medicine_ids.</p><p></p><p>medicine_ids should contain at least 1 medicine_ids.</p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 15 (medicines)</p><p></p><p>Example:</p><p>["otUfMtG4nIpWSc+oWoX7Lw=="]</p>                           |
| latitude                                        | Number | Latitude of the customer                                                                                                                                                                                                                                 |
| longitude                                       | Number | Longitude of the customer                                                                                                                                                                                                                                |
| full\_address                                   | String | <p>Required If lat-long is not provided. This address is used to get the lat-long to find the nearest pharmacy store.</p><p></p><p>Only zipcode can also be passed in this param.</p><p></p><p>like <code>{ "full_address": "560008" }</code></p><p></p> |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-02-15 12:33:58",
    "data": {
        "availability": [
            {
                "medicine_id": "y8P5ElKQqfn/Dkb0uhE9Sg==",
                "in_stock": "yes"
            },
            {
                "medicine_id": "+ZqERHcCTAeuxsJheIXjyw==",
                "in_stock": "no",
                "alternatives": []
            },
            {
                "medicine_id": "I446Nql4z13v8fTxtjx63g==",
                "in_stock": "no",
                "alternatives": [
                    {
                        "medicine_id": "y8P5ElKQqfn/Dkb0uhE9Sg==",
                        "medicine_name": "Ltk 50 Tablet",
                        "mrp": 50,
                        "packing_size": "1 Strip of  10 Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "content": "Losartan (50mg)"
                    }
                ]
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
