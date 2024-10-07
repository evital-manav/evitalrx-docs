---
description: To get alternate products by unique medicine Id.
---

# Branded to Generic



<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/branded_to_generic`

Get Alternate medicines with the best in terms of Expiry, Margin, and Price.

#### Request Body

| Name                                            | Type              | Description                                                                                                                                                                                                                   |
| ----------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>        | String            | Authentication Token                                                                                                                                                                                                          |
| medicine\_ids<mark style="color:red;">\*</mark> | Stringified Array | <p>Array of medicine_ids in the form data</p><p></p><p>[\"eGMwtMdst4OkfNrNoAFxRw\",  \"77eruTI3h1JUg4RqaV20JQ\=="]</p>                                                                                                        |
| order\_by                                       | String            | <p>must be one of <strong>epm, mep, pem</strong></p><p></p><p><strong>epm</strong>: Expiry -> Price -> Margin</p><p><strong>mep</strong>: Margin -> Expiry -> Price</p><p><strong>pem</strong>: Price -> Expiry -> Margin</p> |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-11-17 10:30:42",
    "data": {
        "eGMwtMdst4OkfNrNoAFxRw==": {
            "data": [],
            "message": "alternative not found",
            "status": 0
        },
        "77eruTI3h1JUg4RqaV20JQ==": {
            "data": [
                {
                    "mrp": 204.97,
                    "batch": "C2VAV19",
                    "expiry": "11-23",
                    "packing_size": "1 Bottle of  5 Ml",
                    "medicine_name": "Moxicip D Eye Drop",
                    "manufacturer_name": "Cipla Ltd",
                    "margin_percentage": "23.20",
                    "medicine_id": "M1AGVZYv89bWlk7/oWbG4Q=="
                }
            ],
            "message": "success",
            "status": 1
        }
    }
}
```
{% endtab %}

{% tab title="200: OK No Medicines found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-08 16:20:45",
    "data": {
        "1iFlObGAoedKDQW27+2EQw==": {
            "data": [],
            "message": "alternative not found",
            "status": 0
        }
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid medicine key",
    "datetime": "2022-12-07 11:24:25",
    "data": null
}
```
{% endtab %}
{% endtabs %}
