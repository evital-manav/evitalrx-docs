---
description: Get the Product categories list.
---

# Get Entity Categories

## Get Entity Categories

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/get_entity_categories`

#### Request Body

| Name                                     | Type   | Description          |
| ---------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token |

{% tabs %}
{% tab title="200: OK Categories Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-12-06 11:38:23",
    "data": {
        "results": [
            {
                "id": "BPuoYPiBInH/hiFVTaXQ3Q==",
                "category_name": "Ayurvedic"
            },
            {
                "id": "ptl5OssDd8T9t0WhP7Ku/A==",
                "category_name": "Cosmetic"
            },
            {
                "id": "ROA4bs2F/srPmDmekG6UWQ==",
                "category_name": "Drug"
            },
            {
                "id": "b+mbNHcQX3D95IhpKB8yfQ==",
                "category_name": "Generic"
            },
            {
                "id": "qzT86Go+4cYCJi6FS62LTg==",
                "category_name": "Nutraceuticals"
            },
            {
                "id": "ErCEsS9EooYCSZL+R+fU/g==",
                "category_name": "Otc"
            },
            {
                "id": "nLa7ultHvZaKwyETDWDYpw==",
                "category_name": "Surgical"
            }
        ]
    }
```
{% endtab %}
{% endtabs %}
