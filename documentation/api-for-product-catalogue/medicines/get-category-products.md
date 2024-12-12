---
description: Get the Products of a particular category.
---

# Get Category Products

## Get Category Products

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}catalog/medicines/get_category_items`](https://api.evitalrx.in/v1/catalog/medicines/get_category_items)

#### Request Body

| Name                                           | Type   | Description          |
| ---------------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token |
| category\_id<mark style="color:red;">\*</mark> | String | Category ID          |
| page                                           | Number | Default: 1           |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-03 17:50:28",
    "data": {
        "current_page": 1,
        "rpp": 10,
        "results": [
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "MamyPoko Standard Pants L",
                "content": "",
                "mrp": 195,
                "medicine_id": "PUe/q5mC00cuci4cVAgiWg==",
                "packing_size": "1 Packet of  17 Piece",
                "size": 1,
                "manufacturer_name": "Unicharm India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6286077028b09.jpg"
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "MamyPoko Standard Pants L",
                "content": "",
                "mrp": 195,
                "medicine_id": "PUe/q5mC00cuci4cVAgiWg==",
                "packing_size": "1 Packet of  17 Piece",
                "size": 1,
                "manufacturer_name": "Unicharm India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6286077028b09.jpg"
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "MamyPoko Extra Absorb Pants L",
                "content": "",
                "mrp": 30,
                "medicine_id": "8orluEHZ13mtYr/kNuhTlA==",
                "packing_size": "1 Packet of  2 Piece",
                "size": 1,
                "manufacturer_name": "Unicharm India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/62a87226034ff.jpg"
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "MamyPoko Extra Absorb Pants L",
                "content": "",
                "mrp": 30,
                "medicine_id": "8orluEHZ13mtYr/kNuhTlA==",
                "packing_size": "1 Packet of  2 Piece",
                "size": 1,
                "manufacturer_name": "Unicharm India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/62a87226034ff.jpg"
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "Dove Baby Lotion Rich Moisture",
                "content": "",
                "mrp": 65,
                "medicine_id": "SfplmQsHVjJsp3tv4qlMIQ==",
                "packing_size": "1 Bottle of  1 Gm",
                "size": 1,
                "manufacturer_name": "Unilever India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/63be802b49ab8.jpg"
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "Dove Baby Lotion Rich Moisture",
                "content": "",
                "mrp": 65,
                "medicine_id": "SfplmQsHVjJsp3tv4qlMIQ==",
                "packing_size": "1 Bottle of  1 Gm",
                "size": 1,
                "manufacturer_name": "Unilever India",
                "medicine_type": "otc",
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/63be802b49ab8.jpg"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Products not found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-03 18:03:06",
    "data": {
        "current_page": 4,
        "rpp": 10,
        "results": []
    }
}
```
{% endtab %}

{% tab title="200: OK Validation error" %}
```json
{
    "status_code": "0",
    "status_message": "category_id is required",
    "datetime": "2023-10-03 18:03:24",
    "data": null
}
```
{% endtab %}
{% endtabs %}
