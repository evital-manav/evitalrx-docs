---
description: To add patients with mobile number, name and address.
---

# Add Patient

### <img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Learn How to Add a Patient or Family Member](https://youtu.be/voc4bcyhZ_8?si=Nf_SpvsQX9vVo26v)

## Add Patient

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}doctor/patients/add`](https://api.evitalrx.in/v1/doctor/patients/add)

#### Request Body

| Name                                          | Type   | Description                                                                                                                          |
| --------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| mobile<mark style="color:red;">\*</mark>      | Number | Mobile number of Patient                                                                                                             |
| first\_name<mark style="color:red;">\*</mark> | String | First name of Patient                                                                                                                |
| last\_name<mark style="color:red;">\*</mark>  | String | Last name of Patient                                                                                                                 |
| zipcode                                       | Number | Zipcode of the patient                                                                                                               |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                 |
| dob                                           | String | <p>Date of Birth of the Patient </p><p>Format: YYYY-MM-DD</p>                                                                        |
| gender                                        | String | Gender of the Patient.Must be one of **male, female, other**.                                                                        |
| blood\_group                                  | String | Blood Group of the Patient                                                                                                           |
| custom\_fields                                | Object | <p>Key value pairs of attribute_key and it's value.<br>For ex:<br>{"patient_ipd_id": "IPD1234", "patient_mapped_id": "PMID9876"}</p> |



{% tabs %}
{% tab title="200: OK Patient added successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Patient registered successfully.",
    "datetime": "2025-01-29 11:51:06",
    "version": "1.1.17",
    "data": {
        "patient_id": "iQJtsq0ypLhX11C0NCHQig==" // Uniquue ID of the Patient
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
