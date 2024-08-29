---
description: To reset password with mobile OTP
---

# Reset password

## &#x20;&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/login/reset_password`

#### Request Body

| Name                                       | Type   | Description                              |
| ------------------------------------------ | ------ | ---------------------------------------- |
| apikey<mark style="color:red;">\*</mark>   | String | Authentication token                     |
| mobile<mark style="color:red;">\*</mark>   | Number | Patient's registered mobile              |
| otp<mark style="color:red;">\*</mark>      | String | OTP sent in Forget password send OTP API |
| password<mark style="color:red;">\*</mark> | String | New password                             |

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
    "status_message": "Invalid OTP",
    "datetime": "2023-10-27 18:34:13",
    "data": null
}
```
{% endtab %}
{% endtabs %}

