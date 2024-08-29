---
description: Get the Products of a particular category.
---

# Get Entity Category Products

## Get Entity Category Products

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/get_entity_category_items`

#### Request Body

| Name                                           | Type    | Description                                                          |
| ---------------------------------------------- | ------- | -------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String  | Authentication token                                                 |
| category\_id<mark style="color:red;">\*</mark> | String  | Category ID                                                          |
| page                                           | Number  | Default: 1                                                           |
| in\_stock                                      | Boolean | <p>Fetch products which quantity > 0</p><p></p><p>Default: False</p> |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-12-06 11:32:16",
    "data": {
        "rpp": 20,
        "page": 1,
        "results": [
            {
                "medicine_id": "eigAkZJoGSieolaaX3NQyw==",
                "medicine_name": "Abhyarishta",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
                "content": "",
                "mrp": 145,
                "size": 1,
                "manufacturer_name": "Dabur India Ltd",
                "packing_size": "1 Bottle of  450 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg"
            },
            {
                "medicine_id": "tlHmYY/hZedugQ3z5HDqJg==",
                "medicine_name": "Adliv Syrup",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/60267df21f7f3.jpg",
                "content": "",
                "mrp": 141.47,
                "size": 1,
                "manufacturer_name": "Albert David Ltd",
                "packing_size": "1 Bottle of  200 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 2,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/60267df21f7f3.jpg"
            },
            {
                "medicine_id": "1V+aarul264irQjsWrdxKQ==",
                "medicine_name": "Amla Aloevera With Wheat Grass Juice",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
                "content": "",
                "mrp": 100,
                "size": 1,
                "manufacturer_name": "Patanjali Ayurved Limited",
                "packing_size": "1 Bottle of  500 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg"
            },
            {
                "medicine_id": "kGa0jbMBLLwXE5vChNMU0Q==",
                "medicine_name": "Amla Juice",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/63737ef84ba35.jpg",
                "content": "",
                "mrp": 130,
                "size": 1,
                "manufacturer_name": "Patanjali Ayurved Limited",
                "packing_size": "1 Bottle of  1 Ltr",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 1,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/63737ef84ba35.jpg"
            },
            {
                "medicine_id": "vqhY4vd+iRFVDCojGdzRAQ==",
                "medicine_name": "Amritarishta",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6172a3ff68a65.jpg",
                "content": "",
                "mrp": 195,
                "size": 1,
                "manufacturer_name": "Shree Baidyanath Ayurved Bhawan Pvt Ltd",
                "packing_size": "1 Bottle of  450 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/6172a3ff68a65.jpg"
            },
            {
                "medicine_id": "t1POz3Z1zg5YFEnCq0ra5g==",
                "medicine_name": "Amritdhara",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/623994706c650.jpg",
                "content": "",
                "mrp": 40,
                "size": 1,
                "manufacturer_name": "Amritdhara Pharmacy Pvt Ltd",
                "packing_size": "1 Bottle of  6 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/623994706c650.jpg"
            },
            {
                "medicine_id": "nbKM7Lz4E3vKcpUTMZjNcA==",
                "medicine_name": "Amroid Tablet",
                "dosage_type": "tablet",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
                "content": "",
                "mrp": 237,
                "size": 30,
                "manufacturer_name": "Aimil Pharmaceuticals India Ltd",
                "packing_size": "1 Strip of  30 Tablet",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 60,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg"
            },
            {
                "medicine_id": "BK3MnOw+EWsuqZKXCsRxjw==",
                "medicine_name": "Amrutanjan Advanced Back Pain Roll-ON",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/64def3d405908.jpg",
                "content": "",
                "mrp": 100,
                "size": 1,
                "manufacturer_name": "Amrutanjan Health Care Ltd",
                "packing_size": "1 Bottle of  50 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/64def3d405908.jpg"
            },
            {
                "medicine_id": "pV7oEAMhNTbNPcHoGGVRFA==",
                "medicine_name": "Amrutanjan Extra Power Pain Balm",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6481896859bc5.jpg",
                "content": "",
                "mrp": 40,
                "size": 1,
                "manufacturer_name": "Amrutanjan Health Care Ltd",
                "packing_size": "1 Bottle of  8 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/6481896859bc5.jpg"
            },
            {
                "medicine_id": "6wplHt5TTl/+UDDGXQLHWQ==",
                "medicine_name": "Amyron Syrup",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/5fa0e59499fad.jpg",
                "content": "",
                "mrp": 198,
                "size": 1,
                "manufacturer_name": "Aimil Pharmaceuticals India Ltd",
                "packing_size": "1 Bottle of  200 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 7,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/5fa0e59499fad.jpg"
            },
            {
                "medicine_id": "r8hEggxoKadqpGmsH/mgoA==",
                "medicine_name": "Aptiheal Syrup",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6374d57966790.jpg",
                "content": "",
                "mrp": 145,
                "size": 1,
                "manufacturer_name": "Vigilant Life Sciences Pvt Ltd",
                "packing_size": "1 Bottle of  200 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 1,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/6374d57966790.jpg"
            },
            {
                "medicine_id": "7epdtl6d4YmiDqXsmrVUlA==",
                "medicine_name": "Arodent Gum & Dental Paste",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/617d2764cce0c.jpg",
                "content": "",
                "mrp": 223,
                "size": 1,
                "manufacturer_name": "Ipsa Labs Pvt Ltd",
                "packing_size": "1 Tube of  200 Gm",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 1,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/617d2764cce0c.jpg"
            },
            {
                "medicine_id": "WcAssStbXxQj5wwt/Hj6xA==",
                "medicine_name": "Ashokarishta",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6229d29ec6c31.jpg",
                "content": "",
                "mrp": 137,
                "size": 1,
                "manufacturer_name": "Shree Baidyanath Ayurved Bhawan Pvt Ltd",
                "packing_size": "1 Bottle of  450 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/6229d29ec6c31.jpg"
            },
            {
                "medicine_id": "gLVl1BbBQmu+ZIGPCqndWA==",
                "medicine_name": "Ashokarishta",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/62d68c820e9dc.jpg",
                "content": "",
                "mrp": 115,
                "size": 1,
                "manufacturer_name": "Dabur India Ltd",
                "packing_size": "1 Bottle of  450 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 2,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/62d68c820e9dc.jpg"
            },
            {
                "medicine_id": "+4jNNVc3rdvT5XlzXMizow==",
                "medicine_name": "Ayush Kwath Tablet",
                "dosage_type": "tablet",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/63a5c2c2469fc.jpg",
                "content": "",
                "mrp": 200,
                "size": 60,
                "manufacturer_name": "Shree Baidyanath Ayurved Bhawan Pvt Ltd",
                "packing_size": "1 Bottle of  60 Tablet",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 120,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/63a5c2c2469fc.jpg"
            },
            {
                "medicine_id": "NdOF1yXYndq22dDVwzXfNQ==",
                "medicine_name": "Baidyanath Chandraprabha Bati",
                "dosage_type": "tablet",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/608296c17badf.jpg",
                "content": "",
                "mrp": 100,
                "size": 50,
                "manufacturer_name": "Shree Baidyanath Ayurved Bhawan Pvt Ltd",
                "packing_size": "1 Bottle of  50 Tablet",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 50,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/608296c17badf.jpg"
            },
            {
                "medicine_id": "vssohCb7WxCDolgcHguo/w==",
                "medicine_name": "Baidyanath (Jhansi) Bilva Tail",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/60c73865b7bb6.jpg",
                "content": "",
                "mrp": 120,
                "size": 1,
                "manufacturer_name": "Baidyanath Ayurved Bpvtltd",
                "packing_size": "1 Bottle of  25 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 1,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/60c73865b7bb6.jpg"
            },
            {
                "medicine_id": "/BgA059dxxbgWgV3hfrJ3w==",
                "medicine_name": "Baidyanath Rogan Badam Shirin",
                "dosage_type": "",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/616408099645b.jpg",
                "content": "",
                "mrp": 385,
                "size": 1,
                "manufacturer_name": "Shree Baidyanath Ayurved Bhawan Pvt Ltd",
                "packing_size": "1 Bottle of  100 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 0,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/616408099645b.jpg"
            },
            {
                "medicine_id": "EJohZPYdCh1E4c0FEWq6BQ==",
                "medicine_name": "Bonnisan Drop",
                "dosage_type": "drop",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/601a949fed957.jpg",
                "content": "",
                "mrp": 65,
                "size": 1,
                "manufacturer_name": "Himalaya Drug Company",
                "packing_size": "1 Bottle of  30 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 2,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/601a949fed957.jpg"
            },
            {
                "medicine_id": "1tsVU6T2DUrWLmZ3t93LkA==",
                "medicine_name": "Bonnisan Liquid",
                "dosage_type": "syrup",
                "is_rx_required": 0,
                "image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/6527947559b95.jpg",
                "content": "",
                "mrp": 55,
                "size": 1,
                "manufacturer_name": "Himalaya Drug Company",
                "packing_size": "1 Bottle of  100 Ml",
                "medicine_type": "otc",
                "salt_content_id": "",
                "loose_quantity": 5,
                "is_inventory_available": "yes",
                "watermark_free_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/itemoriginalcopy/medicines/6527947559b95.jpg"
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
    "datetime": "2023-12-06 11:44:01",
    "data": {
        "rpp": 20,
        "current_page": 10,
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
