---
description: To update a particular custom field using the id.
---

# Update Custom Field

Update a custom field

Below is sample cURL request to update a custom field. Use raw JSON format to call the API. Length of the array while update action should be one only.

{% file src="../.gitbook/assets/sample_curl - update_custom_field.txt" %}

<mark style="color:green;">`POST`</mark>[`{{apiUrl}}custom_fields/add_update_custom_field`](https://api.evitalrx.in/v1/custom_fields/add_update_custom_field)

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                                                                      |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                                                                                                                                             |
| entity                                   | Number | type of the entity                                                                                                                                                                                                                               |
| custom\_fields                           | Array  | <p>Array of custom field object of length one containing id attribute key and module. Update one custom field at a time.<br>For ex:<br>{id: string, attribute_key: string, module: string }<br><br>Valid modules are:<br>sales and customers</p> |
| action                                   | String | update                                                                                                                                                                                                                                           |

{% tabs %}
{% tab title="200 Update success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-09-24 15:14:36",
    "data": null
}
```
{% endtab %}

{% tab title="Invalid update id" %}
```json
{
    "status_code": "0",
    "status_message": "update failed",
    "datetime": "2024-09-24 15:14:36",
    "data": null
}
```
{% endtab %}
{% endtabs %}
