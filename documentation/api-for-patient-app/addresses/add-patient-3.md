# Delete Address

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/addresses/delete`](https://api.evitalrx.in/v1/patient/addresses/delete)

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
    "status_message": "Address deleted successfully",
    "datetime": "2023-10-31 12:16:39",
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

