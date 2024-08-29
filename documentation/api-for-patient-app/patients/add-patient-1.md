---
description: To add patients with mobile number, name and address.
---

# Update Patient



## Update Patient &#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/patients/update`

#### Request Body

| Name                                          | Type   | Description                                                                              |
| --------------------------------------------- | ------ | ---------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                     |
| zipcode                                       | Number | Zip code of the Patient                                                                  |
| first\_name<mark style="color:red;">\*</mark> | String | First name of Patient                                                                    |
| last\_name<mark style="color:red;">\*</mark>  | String | Last name of Patient                                                                     |
| dob                                           | String | <p>Date of Birth of the Patient</p><p>Format: YYYY-MM-DD</p>                             |
| gender                                        | String | <p>Gender of the Patient.</p><p>Must be one of <strong>male, female, other</strong>.</p> |
| blood\_group                                  | String | Blood Group of the Patient                                                               |
| patient\_id<mark style="color:red;">\*</mark> | String | Unique ID of Patient                                                                     |

{% tabs %}
{% tab title="200 Patient updated successfully." %}
```
{
    "status_code": "1",
    "status_message": "Patient updated successfully",
    "datetime": "2022-12-06 18:29:42",
    "data": {
        "patient_id": "qAj4hhwefVxwuZX9nFxHkQ=="
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Patient Key",
    "datetime": "2022-12-06 18:32:59",
    "data": null
}
```
{% endtab %}
{% endtabs %}

