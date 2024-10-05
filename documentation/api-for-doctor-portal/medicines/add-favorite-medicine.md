---
description: This API is for doctors to add their favorite medicine.
---

# Add Favorite Medicine



<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/favorite/add`

#### Request Body

| Name                                     | Type   | Description                            |
| ---------------------------------------- | ------ | -------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication Token                   |
| medicine\_ids                            | String | Form data Array containing medicine id |

{% tabs %}
{% tab title="200: OK Product Retrieved Successfully" %}
```json


{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-09-23 16:35:10",
    "data": {}
}

```
{% endtab %}
{% endtabs %}
