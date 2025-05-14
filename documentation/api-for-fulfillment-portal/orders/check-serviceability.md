---
description: This API is deprecated.
---

# ⛔ Check Serviceability

## Get serviceability check

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/check_serviceability`](https://api.evitalrx.in/v1/fulfillment/orders/checkout)

#### Request Body

| Name                                        | Type   | Description                                                                                                                              |
| ------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication Token                                                                                                                     |
| latitude<mark style="color:red;">\*</mark>  | String | Latitude of the customer                                                                                                                 |
| longitude<mark style="color:red;">\*</mark> | String | Longitude of the customer                                                                                                                |
| zipcode<mark style="color:red;">\*</mark>   | String | Zipcode of the patient                                                                                                                   |
| full\_address                               | String | <p>Full address of  the patient for <br>eg. Office B, 3rd Floor, 4D Square Mall, below PVR Cinema, Motera, Ahmedabad, Gujarat 380005</p> |



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-02-13 19:14:46",
    "version": "1.1.27",
    "data": {
        "serviceable": true
    }
}
```
{% endtab %}

{% tab title="200: OK Invalid params" %}
```json
{
    "status_code": "0",
    "status_message": "mobile is required",
    "datetime": "2025-02-13 19:15:10",
    "version": "1.1.27",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Not Serviceable" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-02-13 19:14:46",
    "version": "1.1.27",
    "data": {
        "serviceable": false
    }
}
```
{% endtab %}
{% endtabs %}
