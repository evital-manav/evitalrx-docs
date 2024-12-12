---
description: To add user defined custom fields with attribute key and module
---

# Add Custom Fields

Add custom fields, Maximum limit for an entity to add custom fields is 20. Below is a sample cURL request to add some custom fields:

{% file src="../.gitbook/assets/sample_curl - add_custom_field.txt" %}

<mark style="color:green;">`POST`</mark>[`{{apiUrl}}custom_fields/add_update_custom_field`](https://api.evitalrx.in/v1/custom_fields/add_update_custom_field)

#### Request Body

| Name                                     | Type   | Description                                                                                                                            |
| ---------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                                   |
| custom\_fields                           | Array  | <p>Array of custom field object<br>For ex:<br>{attribute_key: string, module: string }<br>Valid module are:<br>sales and customers</p> |
| action                                   | String | add                                                                                                                                    |

{% tabs %}
{% tab title="OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 10:36:31",
    "data": null
}
```
{% endtab %}

{% tab title="Limit Error" %}
```json
{
    "status_code": "0",
    "status_message": "Total custom field exceeds limit of 20",
    "datetime": "2024-10-01 10:44:00",
    "data": null
}
```
{% endtab %}
{% endtabs %}
