# Signup

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/login/signup`](https://api.evitalrx.in/v1/patient/login/signup)

Register the Patient in the system.&#x20;

#### Request Body

| Name                                        | Type   | Description                                                                                                                  |
| ------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token                                                                                                         |
| mobile<mark style="color:red;">\*</mark>    | String | Mobile number of Patient                                                                                                     |
| firstname<mark style="color:red;">\*</mark> | String | First name of Patient                                                                                                        |
| lastname                                    | String | Last name of Patient                                                                                                         |
| otp<mark style="color:red;">\*</mark>       | String | Verification OTP sent to customer mobile in Signup send OTP API                                                              |
| password<mark style="color:red;">\*</mark>  | String | Password set by patient                                                                                                      |
| os                                          | String | <p>"web" | "android" | "ios"</p><p></p><p>default: "android"</p><p></p><p>Operating system of mobile patients are using.</p> |
| zipcode                                     | String | <p>Length: 6</p><p></p><p>Patient's pincode</p>                                                                              |

{% tabs %}
{% tab title="200 OTP send successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Registered Successfully",
    "datetime": "2023-10-27 18:17:36",
    "data": {
        "profile_picture": "https://d1tu4pmhr82np8.cloudfront.net/storage/users/placeholder_a.png",
        "patient_id": "+FEWdxQs/6ciAyINkc430A==", // Unique ID of the Patient
        "firstname": "Aman",
        "lastname": "Shukla",
        "mobile": "9033071756",
        "patient_code": "P0001P3",
        "status": "active",
        "zipcode": "380008"
    }
}
```
{% endtab %}

{% tab title="200: OK Patient already exists, kindly login." %}
```json
{
    "status_code": "0",
    "status_message": "This Mobile is already exist.",
    "datetime": "2023-10-27 18:18:19",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "mobile length must be at least 10 characters long",
    "datetime": "2023-10-27 18:18:36",
    "data": null
}
```
{% endtab %}
{% endtabs %}

