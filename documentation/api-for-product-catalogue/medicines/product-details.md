---
description: To get item details in your inventory by unique medicine Id.
---

# Product Details

## Product Details

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}catalog/medicines/view`](https://api.evitalrx.in/v1/catalog/medicines/view)

#### Request Body

| Name                                           | Type   | Description                                                                                                                                                                                                                                                                                                     |
| ---------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication Token                                                                                                                                                                                                                                                                                            |
| medicine\_id<mark style="color:red;">\*</mark> | String | Unique id of the product                                                                                                                                                                                                                                                                                        |
| medicine\_ids                                  | String | <p>Stringified Array of medicine_ids.</p><p></p><p><strong>medicine_id</strong> param is optional, if <strong>medicine_ids</strong> param is passed.</p><p></p><p>medicine_ids should contain at least 2 medicine_ids.</p><p></p><p>Example:</p><p>["z5s5a+e/Cj4ip7sUl2zJFQ==", "otUfMtG4nIpWSc+oWoX7Lw=="]</p> |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 15:46:28",
    "data": {
        "content": "",
        "how_medicine_works": "",
        "how_to_use": "",
        "id": "8Oq/U+AVxuCWtncoxUgtEg==", // medicine_id
        "medicine_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/5f056fbc83c8c.jpg",
        "is_rx_required": 0,
        "dosage_type": "",
        "medicine_name": "Organic Harvest Under Eye Gel",
        "mrp": 595,
        "packing_size": "1 Tube of 15gm",
        "size": 1,
        "manufacturer_name": "Organic Harvest",
        "side_effects": "",
        "alcohol": "",
        "driving": "",
        "kidney": "",
        "lactation": "",
        "liver": "",
        "pregnancy": "",
        "medicine_category": "generic",
        "alternative_results": {
            "in_stock_count": 0,
            "results": [
                {
                    "dosage_type": "",
                    "medicine_name": "Azithral XL 200 Liquid",
                    "content": "Azithromycin  (200mg/5ml)",
                    "mrp": "202.87",
                    "medicine_id": "m7IrSmX+8aSwf1QsTNQwxA==",
                    "packing_size": "1 Bottle of  60 Ml",
                    "size": "1",
                    "manufacturer_name": "Alembic Pharmaceuticals Ltd",
                    "medicine_type": "drug"
                },
                {
                    "dosage_type": "",
                    "medicine_name": "Grocapix M Serum",
                    "content": "Minoxidil (5%w/v)",
                    "mrp": "995",
                    "medicine_id": "PwV4BmXVlNv38hazbjPZog==",
                    "packing_size": "1 Bottle of  60 Ml",
                    "size": "1",
                    "manufacturer_name": "Alembic Pharmaceuticals Ltd",
                    "medicine_type": "drug"
                },
                {
                    "dosage_type": "",
                    "medicine_name": "Lamiwin 500 mg Infusion",
                    "content": "Levofloxacin (500mg)",
                    "mrp": "120",
                    "medicine_id": "FH8RZwkCHnVoLQ17auLIjg==",
                    "packing_size": "100 ml in 1 bottle",
                    "size": "1",
                    "manufacturer_name": "Alembic Pharmaceuticals Ltd",
                    "medicine_type": "drug",
                    "schedule_type": "H1"
                }
            ]
        },
        "medicine_images": [
            {
                "medicine_image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/5f056fbc83c8c.jpg",
                "default": "no"
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK No Product found according to request params" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid medicine key",
    "datetime": "2022-12-06 16:42:59",
    "data": null
}
```
{% endtab %}
{% endtabs %}
