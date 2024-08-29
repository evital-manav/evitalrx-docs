---
description: To search manufacturer by name.
---

# Search Manufacturer

## Search Manufacturer

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/manufacturer/search`

#### Request Body

| Name                                           | Type   | Description                     |
| ---------------------------------------------- | ------ | ------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token            |
| searchstring<mark style="color:red;">\*</mark> | String | Min: 3 char required i.e. Cipla |



{% tabs %}
{% tab title="200 Records Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-04-27 10:51:14",
    "data": {
        "results": [
            {
                "id": "YDyrP7SQyRGUkTN1WEwkDA==",
                "title": "Cipla Ganric"
            },
            {
                "id": "+QFIphi6M09I9yDfowOCDQ==",
                "title": "Cipla Ltd"
            }
        ]
    }
}

```
{% endtab %}

{% tab title="200: OK No Products found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 15:21:25",
    "data": {
        "results": []
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"searchstring\" length must be greater than or equal to 3 characters long",
    "datetime": "2022-12-06 15:19:58",
    "data": null
}
```
{% endtab %}
{% endtabs %}

