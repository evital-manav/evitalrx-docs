---
description: This API sends verification code to register mobile number to reset password.
---

# Forgot password send OTP



<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/login/forgotpassword_sendotp`

#### Request Body

| Name                                     | Type   | Description                 |
| ---------------------------------------- | ------ | --------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token        |
| mobile<mark style="color:red;">\*</mark> | String | Patient's registered mobile |

{% tabs %}
{% tab title="200 OTP sent successfully" %}
```json
{
    "status_code": "1",
    "status_message": "OTP sent successfully to your mobile number",
    "datetime": "2023-10-27 18:25:19",
    "data": 1
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "mobile length must be at least 10 characters long",
    "datetime": "2023-10-27 18:25:47",
    "data": null
}
```
{% endtab %}
{% endtabs %}

