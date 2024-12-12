---
description: Get the Products of a particular category.
---

# Get Category Products

## Get Category Products

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}patient/medicines/get_category_items`](https://api.evitalrx.in/v1/patient/medicines/get_category_items)

#### Request Body

| Name                                           | Type   | Description                                                                                                                                 |
| ---------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication token                                                                                                                        |
| category\_id<mark style="color:red;">\*</mark> | String | Category ID                                                                                                                                 |
| page                                           | Number | Default: 1                                                                                                                                  |
| show\_sale\_rate                               | String | <p>yes | no</p><p></p><p>Show the product at discounted rate in price attribute, where price = MRP - Discount.</p><p></p><p>Default: no</p> |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-02-08 11:42:55",
    "data": {
        "current_page": 1,
        "rpp": 10,
        "results": [
            {
                "dosage_type": "cream",
                "salt_content_id": "",
                "medicine_name": "Parth Hair Remover Cream",
                "content": "",
                "mrp": 72,
                "medicine_id": "XtZt2tSiOXhZioJZFtbmIQ==",
                "packing_size": "1 Tube of  50 Gm",
                "size": 1,
                "manufacturer_name": "Parth Remedies",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/627b4e20dfae2.jpg",
                "is_inventory_available": "yes",
                "sale_discount": 5,
                "price": 68.4,
                "discount_percentage": 5
            },
            {
                "dosage_type": "cream",
                "salt_content_id": "",
                "medicine_name": "Pediguard Foot Care Cream",
                "content": "",
                "mrp": 85,
                "medicine_id": "PncCV8JIb+BX+U6LGgLwgA==",
                "packing_size": "1 Jar of  30 Gm",
                "size": 1,
                "manufacturer_name": "Ek-Tek Pharma",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/621c9cdeaea85.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 85,
                "discount_percentage": 0
            },
            {
                "dosage_type": "cream",
                "salt_content_id": "",
                "medicine_name": "Olay Natural Aura Glowing Radiance Cream SPF 15",
                "content": "",
                "mrp": 399,
                "medicine_id": "hxNLBwKwDviN/suzsgQldw==",
                "packing_size": "1 Jar of  50 Gm",
                "size": 1,
                "manufacturer_name": "Procter & Gamble Hygiene and Health Care Ltd",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/62186bdce0538.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 399,
                "discount_percentage": 0
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "Dry-Safe Eco Unisex Adult Pants XL",
                "content": "",
                "mrp": 650,
                "medicine_id": "gUsymFemV/3f93L33tdRiw==",
                "packing_size": "1 Packet of  10 Piece",
                "size": 1,
                "manufacturer_name": "Tataria Hygiene",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/6218847788a13.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 650,
                "discount_percentage": 0
            },
            {
                "dosage_type": "powder",
                "salt_content_id": "",
                "medicine_name": "Candid Dusting Powder",
                "content": "",
                "mrp": 26.3,
                "medicine_id": "MrIBe+BRfKjBFeadWzkVMw==",
                "packing_size": "1 Bottle of  30 Gm",
                "size": 1,
                "manufacturer_name": "Glenmark Pharmaceuticals Ltd",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/62395c80da364.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 26.3,
                "discount_percentage": 0
            },
            {
                "dosage_type": "tablet",
                "salt_content_id": "",
                "medicine_name": "Chirivilwadi Kashayam Tablet",
                "content": "",
                "mrp": 47,
                "medicine_id": "zGj3PhY/v6ahX3Oh1qLyog==",
                "packing_size": "1 Strip of  10 Tablet",
                "size": 10,
                "manufacturer_name": "Avn Ayurveda Formulations Pvt Ltd",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/6242dbcd22746.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 47,
                "discount_percentage": 0
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "V Clean Everyday Feminine Hygiene Wash",
                "content": "",
                "mrp": 195,
                "medicine_id": "UalUHpRsQmNHqGcCfnblyg==",
                "packing_size": "1 Bottle of  100 Ml",
                "size": 1,
                "manufacturer_name": "Nukind Healthcare Pvt Ltd",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/622ef1d048b2a.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 195,
                "discount_percentage": 0
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "Huda Beauty Wax Strips With Charcoal Extracts",
                "content": "",
                "mrp": 170,
                "medicine_id": "yBG5nH6HYTK7xW9vTuawWA==",
                "packing_size": "1 Box of  20 Piece",
                "size": 1,
                "manufacturer_name": "Huda Beauty",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/62877ae67ff4e.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 170,
                "discount_percentage": 0
            },
            {
                "dosage_type": "",
                "salt_content_id": "",
                "medicine_name": "Pcreek Vaginal Wash",
                "content": "",
                "mrp": 165,
                "medicine_id": "epw9A/S2n6A3hl3Fzb2+qQ==",
                "packing_size": "1 Bottle of  100 Ml",
                "size": 1,
                "manufacturer_name": "Cubit Healthcare",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/6381dc5fc89c4.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 165,
                "discount_percentage": 0
            },
            {
                "dosage_type": "cream",
                "salt_content_id": "",
                "medicine_name": "Twinkle Hair Remover Cream",
                "content": "",
                "mrp": 60,
                "medicine_id": "NjVsVtPpvjCNRIlz8wSRtg==",
                "packing_size": "1 Tube of  30 Gm",
                "size": 1,
                "manufacturer_name": "Austro Labs Ltd",
                "medicine_type": "otc",
                "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/default.jpg",
                "is_inventory_available": "no",
                "sale_discount": null,
                "price": 60,
                "discount_percentage": 0
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
