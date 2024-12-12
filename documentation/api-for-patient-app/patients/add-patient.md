---
description: To add patients with mobile number, name and address.
---

# Add Patient

### &#x20;<img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Learn How to Add a Patient or Family Member](https://youtu.be/voc4bcyhZ_8?si=Nf_SpvsQX9vVo26v)

### Add Patient

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/patients/add`](https://api.evitalrx.in/v1/patient/patients/add)

#### Request Body

| Name                                          | Type   | Description                                                                                                                          |
| --------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                 |
| zipcode                                       | Number | Zip code of the Patient                                                                                                              |
| mobile<mark style="color:red;">\*</mark>      | String | Mobile number of Patient                                                                                                             |
| first\_name<mark style="color:red;">\*</mark> | String | First name of Patient                                                                                                                |
| last\_name                                    | String | Last name of Patient                                                                                                                 |
| dob                                           | String | <p>Date of Birth of the Patient</p><p>Format: YYYY-MM-DD</p>                                                                         |
| gender                                        | String | <p>Gender of the Patient.</p><p>Must be one of <strong>male, female, other</strong>.</p>                                             |
| blood\_group                                  | String | Blood Group of the Patient                                                                                                           |
| custom\_fields                                | Object | <p>Key value pairs of attribute_key and it's value.<br>For ex:<br>{"patient_ipd_id": "IPD1234", "patient_mapped_id": "PMID9876"}</p> |

{% tabs %}
{% tab title="200 Patient added successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Patient registered successfully.",
    "datetime": "2022-12-06 18:07:04",
    "data": {
        "patient_id": "qAj4hhwefVxwuZX9nFxHkQ==" // Unique Patient ID
    }
}
```
{% endtab %}

{% tab title="200: OK Patient added Failed" %}
```
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

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Please enter valid zipcode",
    "datetime": "2022-12-06 18:09:55",
    "data": null
}
```
{% endtab %}
{% endtabs %}

