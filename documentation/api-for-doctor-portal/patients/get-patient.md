---
description: To get the patient details
---

# Get Patient

## Get Patient

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/patients/view`

#### Request Body

| Name                                          | Type    | Description                                                                                                                   |
| --------------------------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark> | String  | Unique id of the Patient                                                                                                      |
| apikey<mark style="color:red;">\*</mark>      | String  | Authentication token                                                                                                          |
| mobile<mark style="color:red;">\*</mark>      | String  | Either patient\_id or mobile should be passed.                                                                                |
| show\_family\_list                            | Boolean | <p>Default: false</p><p></p><p>If passed true then patient's family member details will be added in the response. </p><p></p> |

{% tabs %}
{% tab title="200: OK Patient retrived successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-01-25 16:07:36",
    "data": [
        {
            "firstname": "Manav",
            "lastname": "Patel",
            "zipcode": "380005",
            "mobile": "9846251658",
            "family_member_list": [
                {
                    "id": "dXuOGHX5xlrfXQkkByAX3g==",
                    "firstname": "Poojan",
                    "lastname": "Mehta",
                    "zipcode": "380005",
                    "mobile": "9887878787"
                },
                {
                    "id": "dXuOGHX5xlrfXQkkByAX3g==",
                    "firstname": "Jay",
                    "lastname": "Patel",
                    "zipcode": "",
                    "mobile": ""
                }
            ],
            "patient_id": "dXuOGHX5xlrfXQkkByAX3g==",
            "custom_fields": {
                "patient_ipd_id": "IPD1234",
                "patient_mapped_id": "PMID9876"
            }
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
    "datetime": "2022-12-07 12:32:04",
    "data": null
}
```
{% endtab %}
{% endtabs %}

## Get Patient

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/patients/view`

#### Request Body

| Name                                          | Type    | Description  |
| --------------------------------------------- | ------- | ------------ |
| patient\_id<mark style="color:red;">\*</mark> | String  | 1A62EQMlDx8t |
| apikey<mark style="color:red;">\*</mark>      | String  | V6oBy7oMFZbX |
| mobile<mark style="color:red;">\*</mark>      | String  | AsD3PhN0mKYs |
| show\_family\_list                            | Boolean | 2dHrkQuS9UDT |
