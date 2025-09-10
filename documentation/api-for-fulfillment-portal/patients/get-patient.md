---
description: To get the patient details
---

# Get Patient

## Get Patient

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/patients/view`](https://dev-api.evitalrx.in/v1/fulfillment/patients/view)

#### Request Body

| Name                                          | Type   | Description                                    |
| --------------------------------------------- | ------ | ---------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark> | String | Unique id of the Patient                       |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                           |
| mobile                                        | String | Either patient\_id or mobile should be passed. |

{% tabs %}
{% tab title="200 Patient details retrieved successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 18:11:54",
    "data": [
        {
            "firstname": "Manav",
            "lastname": "Patel",
            "zipcode": "380008",
            "mobile": "9787998785",
            "patient_id": "qAj4hhwefVxwuZX9nFxHkQ=="
        }
    ]
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"patient_id\" is required",
    "datetime": "2022-12-06 18:12:45",
    "data": null
}
```
{% endtab %}
{% endtabs %}

