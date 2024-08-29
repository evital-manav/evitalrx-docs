---
description: To add patients with mobile number, name and address.
---

# Add Patient

## Add Patient

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/patients/add`

#### Request Body

| Name                                          | Type   | Description                                                   |
| --------------------------------------------- | ------ | ------------------------------------------------------------- |
| mobile<mark style="color:red;">\*</mark>      | Number | Mobile number of Patient                                      |
| first\_name<mark style="color:red;">\*</mark> | String | First name of Patient                                         |
| last\_name<mark style="color:red;">\*</mark>  | String | Last name of Patient                                          |
| zipcode                                       | Number | Zipcode of the patient                                        |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                          |
| dob                                           | String | <p>Date of Birth of the Patient </p><p>Format: YYYY-MM-DD</p> |
| gender                                        | String | Gender of the Patient.Must be one of **male, female, other**. |
| blood\_group                                  | String | Blood Group of the Patient                                    |

{% tabs %}
{% tab title="200: OK Patient added successfully." %}
```json
{
    "status_code": "0",
    "status_message": "This Mobile is already exist.",
    "datetime": "2022-12-07 12:18:55",
    "data": {
        "patient_id": "haaLvntZX7KmadCtJa314w=="
    }
}
```
{% endtab %}

{% tab title="200: OK Patient add Failed" %}
```json
{
    "status_code": "0",
    "status_message": "This Mobile is already exist.",
    "datetime": "2022-12-07 12:23:41",
    "data": {
        "patient_id": "qAj4hhwefVxwuZX9nFxHkQ=="
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Failed" %}
```json
{
    "status_code": "0",
    "status_message": "\"mobile\" is required",
    "datetime": "2022-12-07 12:25:35",
    "data": null
}
```
{% endtab %}
{% endtabs %}
