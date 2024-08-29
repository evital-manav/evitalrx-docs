# Signup send OTP

## &#x20;&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/login/signup_sendotp`

API to check whether the patient should sign up or log in.&#x20;

#### Request Body

| Name                                        | Type   | Description              |
| ------------------------------------------- | ------ | ------------------------ |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token     |
| mobile<mark style="color:red;">\*</mark>    | String | Mobile number of Patient |
| firstname<mark style="color:red;">\*</mark> | String | First name of Patient    |
| lastname                                    | String | Last name of Patient     |

{% tabs %}
{% tab title="200 OTP send successfully." %}
```json
{
    "status_code": "1",
    "status_message": "OTP sent successfully to your mobile number",
    "datetime": "2023-10-25 17:04:47",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Patient already exists, kindly login." %}
```json
{
    "status_code": "0",
    "status_message": "This Mobile is already exist.",
    "datetime": "2023-10-25 17:46:24",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Please enter valid mobile",
    "datetime": "2022-12-06 18:09:55",
    "data": null
}
```
{% endtab %}
{% endtabs %}

