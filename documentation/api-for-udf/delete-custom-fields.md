---
description: To delete custom field using the id.
---

# Delete Custom Fields

Delete one or more custom fields.

Below is a Sample cURL request to delete particular custom fields.

```json
curl --location 'localhost:4000/v1/custom_fields/add_update_custom_field' \
--header 'Content-Type: application/json' \
--data '{
  "apikey":"**************",
  "action": "delete",
  "custom_fields": [
        {
            "id": "5wP6t/dlZrIzNqssQLUUbQ==",
            "attribute_key": "zipcode",
            "module": "customers"
        },
        {
            "id": "iZ4zlQnA1LpIEiZ+i0D25Q==",
            "attribute_key": "prescription_id",
            "module": "customers"
        }
   ]
}
'
```



<mark style="color:green;">`POST`</mark>`https://api.evitalrx.in/v1/custom_fields/add_update_custom_field`

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                    |
| ---------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                                                                                           |
| entity                                   | Number | type of the entity                                                                                                                                                                             |
| custom\_fields                           | Array  | <p>Array of custom field object containing id, attribute key and module name<br>For ex:<br>{id: string, attribute_key: string, module: string}<br>Valid module are:<br>sales and customers</p> |
| action                                   | String | delete                                                                                                                                                                                         |

{% tabs %}
{% tab title="OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 10:24:18",
    "data": null
}
```
{% endtab %}

{% tab title="Invalid id of attribute" %}
```json
{
    "status_code": "0",
    "status_message": "deleting failed",
    "datetime": "2024-10-01 10:25:52",
    "data": null
}
```
{% endtab %}
{% endtabs %}
