---
description: To get all items in your inventory.
---

# Get Inventory Items

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}doctor/medicines/get_inventory_items`](https://api.evitalrx.in/v1/doctor/medicines/get_inventory_items)

#### Request Body

| Name                                     | Type   | Description          |
| ---------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication Token |

{% tabs %}
{% tab title="200: OK Product Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-08 16:52:57",
    "data": [
        {
            "medicine_id": "ZnsQl586DmR/ANT3aLdM4g==",
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "size": 10,
            "packing_size": "10 tablets in 1 strip",
            "mrp": 23.5,
            "medicine_name": "Ltk 50 Tablet",
            "quantity": 100,
            "content": "Losartan (50mg)",
            "dosage_type": "tablet"
        },
        {
            "medicine_id": "tx/SXzkiaaHjYXAFRCvN8Q==",
            "manufacturer_name": "GlaxoSmithKline Consumer Healthcare",
            "size": 1,
            "packing_size": "1 Strip of 15 tablets",
            "mrp": 30.24,
            "medicine_name": "Crocin 650mg Tablet",
            "quantity": 10,
            "content": "Paracetamol / Acetaminophen (125mg)",
            "dosage_type": ""
        },
        {
            "medicine_id": "6+ZMmabCAM//aQXT/8hebg==",
            "manufacturer_name": "Abaris Healthcare",
            "size": 1,
            "packing_size": "60 ml in 1 bottle",
            "mrp": 26,
            "medicine_name": "Corflam S Suspension",
            "quantity": 10,
            "content": "Ibuprofen (NA) + Paracetamol / Acetaminophen (NA)",
            "dosage_type": ""
        },
        {
            "medicine_id": "otUfMtG4nIpWSc+oWoX7Lw==",
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "size": 15,
            "packing_size": "1 Strip of  15 Tablet",
            "mrp": 32.9,
            "medicine_name": "LTK-H Tablet 5",
            "quantity": 1380,
            "content": "",
            "dosage_type": ""
        }
    ]
}
```
{% endtab %}
{% endtabs %}
