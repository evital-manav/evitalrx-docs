---
description: Get the Product categories list.
---

# Get Categories

## Get Categories

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}patient/medicines/get_categories`](https://api.evitalrx.in/v1/patient/medicines/get_categories)

#### Request Body

| Name                                     | Type   | Description                                                                                                   |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                          |
| searchstring                             | String | <p>If searchstring passed, it will fetch relevant categories. </p><p>Min len: 3 </p><p>Max len: 20</p><p></p> |
| page                                     | Number | Default: 1                                                                                                    |

{% tabs %}
{% tab title="200: OK Categories Retrieved Successfully" %}
```json

{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-03 17:34:23",
    "data": {
        "current_page": 1,
        "rpp": 5,
        "results": [
            {
                "id": "mB3b+VF0xsD9XnRkj0evHQ==", // Unique ID of the Category
                "category_name": "Personal Care",
                "category_picture": "https://d2ffmswuyj0h1d.cloudfront.net/storage/extra/cosmetic/default.jpg"
            },
            {
                "id": "x+hOdgFr9YalM4JTGrgOhg==",
                "category_name": "Fitness & Supplements",
                "category_picture": "https://d2ffmswuyj0h1d.cloudfront.net/storage/extra/cosmetic/default.jpg"
            },
            {
                "id": "ibqdoR3lz+/fQXQnibWPCA==",
                "category_name": "Health Devices",
                "category_picture": "https://d2ffmswuyj0h1d.cloudfront.net/storage/extra/cosmetic/default.jpg"
            },
            {
                "id": "q7dxGR/3f2J95UbkkQniNA==",
                "category_name": "Pet Care",
                "category_picture": "https://d2ffmswuyj0h1d.cloudfront.net/storage/extra/cosmetic/default.jpg"
            },
            {
                "id": "lCLRl5M5V0FsPEy0b37WUQ==",
                "category_name": "Healthcare Devices",
                "category_picture": "https://d2ffmswuyj0h1d.cloudfront.net/storage/extra/cosmetic/default.jpg"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Categories not found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-03 17:57:39",
    "data": {
        "current_page": 1,
        "rpp": 5,
        "results": []
    }
}
```
{% endtab %}

{% tab title="200: OK Validation error" %}
```json

{
    "status_code": "0",
    "status_message": "searchstring length must be at least 3 characters long",
    "datetime": "2023-10-03 17:58:07",
    "data": null
}
```
{% endtab %}
{% endtabs %}
