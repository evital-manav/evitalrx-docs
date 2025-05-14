---
description: To check if a location is serviceable
---

# Check Serviceability V3

## Get serviceability check

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/check_serviceability_v3`](https://api.evitalrx.in/v1/fulfillment/orders/check_serviceability_v3)

#### Request Body

| Name                                            | Type   | Description                                                                                                                              |
| ----------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>        | String | Authentication Token                                                                                                                     |
| latitude<mark style="color:red;">\*</mark>      | String | Latitude of the customer                                                                                                                 |
| longitude<mark style="color:red;">\*</mark>     | String | Longitude of the customer                                                                                                                |
| zipcode<mark style="color:red;">\*</mark>       | String | Zipcode of the patient                                                                                                                   |
| service\_type<mark style="color:red;">\*</mark> | String | <p>Service includes "quick", "regular", "same_day" and "pan_india"</p><p>For eg.<br>["regular","same_day"]</p>                          |
| full\_address                                   | String | <p>Full address of  the patient for <br>eg. Office B, 3rd Floor, 4D Square Mall, below PVR Cinema, Motera, Ahmedabad, Gujarat 380005</p> |



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-05-14 10:22:04",
    "version": "1.1.133",
    "data": {
        "quick": null,
        "regular": {
            "serviceable": true,
            "error_slug": "",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLVm6SiC2t0JAqdfTAkYsDVYnjO35Tp80VHQ/aZ9mWsGRs0y47uR97JYB5QvSDMltGUXuEppfksSED8isKapydaYzu+gfqX/0pH9syqVpDt2KL1tjCG+YhTdGeHuHDTKfOvFXtcAzEMOHWEOr8sSvnT4="
        },
        "same_day": {
            "serviceable": true,
            "error_slug": "",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLeGCJnWMLSOhvviSlR4mPlwrfwFot7T7TaVdW3JvgTd9C6SfulvWvA9nNXXXp2J3cNEKLbLvMJwhxzTgAWUP8wrGBBL2ONKI3DD/wx9lNM2R+5utflMGYgl6kuZ3zfZlEQz4Bz9yNzOTirPgVMYw/7A="
        },
        "pan_india": null
    }
}
```
{% endtab %}

{% tab title="200: OK Invalid params" %}
```json
{
    "status_code": "0",
    "status_message": "zipcode is required",
    "datetime": "2025-05-14 10:22:41",
    "version": "1.1.133",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Not Serviceable" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-05-14 10:23:22",
    "version": "1.1.133",
    "data": {
        "quick": null,
        "regular": {
            "serviceable": false,
            "error_slug": "no_pharmacy_found",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLVm6SiC2t0JAqdfTAkYsDVaIW1ItSdS37OKMQ5miSYjf"
        },
        "same_day": {
            "serviceable": false,
            "error_slug": "no_pharmacy_found",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLeGCJnWMLSOhvviSlR4mPlyTurNYbuWd2jb5dWPzlIj5"
        },
        "pan_india": null
    }
}
```
{% endtab %}
{% endtabs %}
