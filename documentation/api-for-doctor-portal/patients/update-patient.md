---
description: To Update patient with mobile number, name and address.
---

# Update Patient

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/patients/update`

#### Request Body

| Name                                          | Type   | Description                                                   |
| --------------------------------------------- | ------ | ------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark> | String | Unique ID of the patient.                                     |
| first\_name<mark style="color:red;">\*</mark> | String | First name of Patient                                         |
| last\_name<mark style="color:red;">\*</mark>  | String | Last name of Patient                                          |
| zipcode                                       | Number | Zipcode of the patient                                        |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                          |
| dob                                           | String | <p>Date of Birth of the Patient </p><p>Format: YYYY-MM-DD</p> |
| gender                                        | String | Gender of the Patient.Must be one of **male, female, other**. |
| blood\_group                                  | String | Blood Group of the Patient                                    |

{% tabs %}
{% tab title="200: OK Patient updated successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Patient updated successfully",
    "datetime": "2022-12-08 17:27:43",
    "data": {
        "patient_id": "haaLvntZX7KmadCtJa314w=="
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Failed" %}
```json
{
    "status_code": "0",
    "status_message": "\"patient_id\" is required",
    "datetime": "2022-12-07 12:25:35",
    "data": null
}
```
{% endtab %}
{% endtabs %}
