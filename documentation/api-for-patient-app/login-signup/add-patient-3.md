---
description: To change password
---

# Change password

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/login/change_password`](https://api.evitalrx.in/v1/patient/login/change_password)

#### Request Body

| Name                                            | Type   | Description          |
| ----------------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark>        | String | Authentication token |
| patient\_id<mark style="color:red;">\*</mark>   | String | Unique ID of patient |
| new\_password<mark style="color:red;">\*</mark> | String | New password         |
| old\_password<mark style="color:red;">\*</mark> | String | Existing password    |

{% tabs %}
{% tab title="200: OK Password Updated Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Password Updated Successfully",
    "datetime": "2023-10-27 18:35:45",
    "data": 1
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Old Password is Incorrect",
    "datetime": "2023-10-27 20:11:05",
    "data": null
}
```
{% endtab %}
{% endtabs %}

