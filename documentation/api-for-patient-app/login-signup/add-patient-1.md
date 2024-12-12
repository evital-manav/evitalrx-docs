---
description: Login with mobile & password
---

# Login

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/login`](https://api.evitalrx.in/v1/patient/login)

#### Request Body

| Name                                       | Type   | Description          |
| ------------------------------------------ | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark>   | String | Authentication token |
| mobile<mark style="color:red;">\*</mark>   | String | Patient's mobile     |
| password<mark style="color:red;">\*</mark> | String | Patient's password   |

{% tabs %}
{% tab title="200 Logged In Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Logged In Successfully",
    "datetime": "2023-10-27 18:19:12",
    "data": {
        "patient_id": "8aBVYpYlBc13aSmG4vTJTQ==",
        "status": "active",
        "accesstoken": "vTjMEeTh3ZOMFEPp",
        "profile_picture": "https://d1tu4pmhr82np8.cloudfront.net/storage/users/placeholder_a.png",
        "firstname": "Aman",
        "lastname": "Shukla",
        "patient_code": "P0001P0",
        "zipcode": "380008"
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Mobile or Password.",
    "datetime": "2023-10-27 18:21:50",
    "data": null
}
```
{% endtab %}
{% endtabs %}

