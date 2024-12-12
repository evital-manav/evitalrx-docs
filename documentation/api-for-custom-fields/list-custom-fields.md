---
description: To list the user defined custom fields.
---

# List Custom Fields

List custom fields

Below is a sample cURL to list custom fields.

{% file src="../.gitbook/assets/sample_curl - list_custom_fields.txt" %}

<mark style="color:green;">`POST`</mark>[`{{apiUrl}}custom_fields/`list\_user\_custom\_fields](https://api.evitalrx.in/v1/custom_fields/list_user_custom_fields)

#### Request Body

| Name                                     | Type   | Description                                                                                                                    |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                           |
| module                                   | String | <p>Type of module,</p><p>Valid module are:</p><p>sales and customers.</p><p>if not provided all module fields are listed, </p> |



{% tabs %}
{% tab title="OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-09-30 17:04:42",
    "data": [
        {
            "id": "oyESErpn5eM/lQZPgEvxRw==",
            "attribute_key": "prescription_id",
            "module": "sales"
        },
        {
            "id": "J7kwRmvgO/93drQrS09DjA==",
            "attribute_key": "appointment_id",
            "module": "sales"
        },
        {
            "id": "zZBjQtv8YC8gzeDpmzakxg==",
            "attribute_key": "zipcode",
            "module": "sales"
        }
    ]
}
```
{% endtab %}

{% tab title="404 Invalid API key" %}
```json
{
    "status_code": "404",
    "status_message": "Invalid API Key",
    "datetime": "2024-09-30 17:11:28",
    "data": null
}
```
{% endtab %}
{% endtabs %}
