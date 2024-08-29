# Set Default Address

## &#x20;&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/addresses/set_default`

#### Request Body

| Name                                          | Type   | Description          |
| --------------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token |
| patient\_id<mark style="color:red;">\*</mark> | String | Unique ID of patient |
| address\_id<mark style="color:red;">\*</mark> | String | Unique ID of address |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Set as Default successfully",
    "datetime": "2023-10-31 11:55:36",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Patient Key",
    "datetime": "2023-10-31 10:57:03",
    "data": null
}
```
{% endtab %}
{% endtabs %}

