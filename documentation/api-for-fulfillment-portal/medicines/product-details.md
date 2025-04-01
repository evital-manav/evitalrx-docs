---
description: To get item details in your inventory by unique medicine Id.
---

# Product Details

## Product Details

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/medicines/view`](https://api.evitalrx.in/v1/fulfillment/medicines/view)

#### Request Body

| Name                                           | Type   | Description                                                                                                                                                                                                                                                                                                     |
| ---------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication Token                                                                                                                                                                                                                                                                                            |
| medicine\_id<mark style="color:red;">\*</mark> | String | Unique id of the product                                                                                                                                                                                                                                                                                        |
| medicine\_ids                                  | String | <p>Stringified Array of medicine_ids.</p><p></p><p><strong>medicine_id</strong> param is optional, if <strong>medicine_ids</strong> param is passed.</p><p></p><p>medicine_ids should contain at least 2 medicine_ids.</p><p></p><p>Example:</p><p>["z5s5a+e/Cj4ip7sUl2zJFQ==", "otUfMtG4nIpWSc+oWoX7Lw=="]</p> |
| latitude                                       | Number | Latitude of the customer                                                                                                                                                                                                                                                                                        |
| longitude                                      | Number | Longitude of the customer                                                                                                                                                                                                                                                                                       |
| distance                                       | Number | <p>Distance of fulfillment.</p><p></p><p>radius of search area for search provided item</p>                                                                                                                                                                                                                     |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-04-01 12:30:34",
    "version": "1.1.89",
    "data": {
        "content": "Losartan (50mg)",
        "how_medicine_works": "Ltk 50 Tablet is an angiotensin receptor blocker (ARB). It relaxes blood vessel by blocking the action of a chemical that usually makes blood vessels tighter. This lowers the blood pressure, allowing the blood to flow more smoothly to different organs and the heart to pump more efficiently.",
        "how_to_use": "Take this medicine in the dose and duration as advised by your doctor. Swallow it as a whole. Do not chew, crush or break it. Ltk 50 Tablet may be taken with or without food, but it is better to take it at a fixed time.",
        "id": "y1sw0N315wy4+UDhhT5FjA==",
        "medicine_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/6142edda9e799.jpeg",
        "is_rx_required": 0,
        "dosage_type": "tablet",
        "medicine_name": "Ltk 50 Tablet",
        "mrp": 23.5,
        "packing_size": "1 Strip of  10 Tablet",
        "pack_size": "10 Tablet",
        "packing": "Strip",
        "size": 10,
        "hsn_code": "10001111",
        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
        "side_effects": " Common   Dizziness  Back pain  Sinus inflammation  Increased potassium level in blood  ",
        "alcohol": "Taking Losartan with alcohol may excessively lower the blood pressure.",
        "driving": "It is not known whether Ltk 50 Tablet alters the ability to drive. Do not drive if you experience any symptoms that affect your ability to concentrate and react.",
        "kidney": "Ltk 50 Tablet is safe to use in patients with kidney disease. No dose adjustment of Ltk 50 Tablet is recommended.<br>However, talk to your doctor if you have any underlying kidney disease. Regular monitoring of blood pressure is recommended for better dose adjustment.",
        "lactation": "Ltk 50 Tablet is probably safe to use during lactation.  Limited human data suggests that the drug does not represent a significant risk to the baby.",
        "liver": "Ltk 50 Tablet should be used with caution in patients with liver disease. Dose adjustment of Ltk 50 Tablet may be needed. Please consult your doctor.<br>Use of Ltk 50 Tablet is not recommended in patients with severe liver disease.",
        "pregnancy": "Ltk 50 Tablet is unsafe to use during pregnancy.<br>There is positive evidence of human fetal risk, but the benefits from use in pregnant women may be acceptable despite the risk, for example in life-threatening situations. Please consult your doctor.",
        "medicine_category": "drug",
        "gst_percentage": 12,
        "medicine_type": 65,
        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/6142edda9e799.jpeg",
        "price": 21.15,
        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
        "other_packings": "",
        "salt_content_id": "SBFG1vyLxuS3eapamEiruQ==",
        "schedule_type": "",
        "discount_percentage": 10,
        "in_stock": false,
        "size_variants": [],
        "size_variants_2": [],
        "alternative_results": {
            "results": [],
            "is_salt_content_id_zero": false
        },
        "medicine_images": [],
        "thumb_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/6142edda9e799.jpeg",
        "thumb_medicine_image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/6142edda9e799.jpeg"
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

{% tab title="200: OK Multiple Medicines" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 17:54:14",
    "data": [
        {
            "content": "",
            "how_medicine_works": "LTK-H Tablet is a combination of two medicines: Losartan and Hydrochlorothiazide, which lowers the blood pressure effectively. Losartan is an angiotensin receptor blocker (ARB). It works by blocking the hormone angiotensin thereby relaxing blood vessels. This allows the blood to flow more smoothly and the heart to pump more efficiently. Hydrochlorothiazide is a diuretic that removes extra water and certain electrolytes from the body. Over time it also relaxes blood vessels and improves blood flow.",
            "how_to_use": "Take this medicine in the dose and duration as advised by your doctor. Swallow it as a whole. Do not chew, crush or break it. LTK-H Tablet may be taken with or without food, but it is better to take it at a fixed time.",
            "id": "otUfMtG4nIpWSc+oWoX7Lw==",
            "medicine_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/611c99c173648.jpg",
            "is_rx_required": 1,
            "dosage_type": "",
            "medicine_name": "LTK-H Tablet 5",
            "mrp": 24,
            "packing_size": "1 Strip of  15 Tablet",
            "size": 15,
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "side_effects": " Common   Nausea  Taste change  Stomach upset  Diarrhea  Headache  Dizziness  Weakness  Decreased blood pressure  Increased blood uric acid  Increased blood lipid level  Glucose intolerance  Electrolyte imbalance  ",
            "medicine_category": "otc",
            "loose_quantity": 1305,
            "sale_discount": 0,
            "strip_quantity": 87,
            "is_inventory_available": "yes",
            "price": 24,
            "sell_in_loose": "yes",
            "warning_details": [
                {
                    "liver": "LTK-H Tablet should be used with caution in patients with liver disease. Dose adjustment of LTK-H Tablet may be needed. Please consult your doctor."
                },
                {
                    "alcohol": "Taking Hydrochlorothiazide with alcohol may have additive effects in lowering blood pressure. You may experience headache, dizziness, lightheadedness, fainting, and/or changes in pulse or heart rate."
                },
                {
                    "driving": "LTK-H Tablet may make you feel dizzy, sleepy, tired, or decrease alertness. If this happens, do not drive."
                },
                {
                    "kidney": "LTK-H Tablet should be used with caution in patients with severe kidney disease. Dose adjustment of LTK-H Tablet may be needed. Please consult your doctor.<br>Use of LTK-H Tablet is not recommended in patients with severe kidney disease."
                },
                {
                    "lactation": "LTK-H Tablet is probably safe to use during lactation.  Limited human data suggests that the drug does not represent a significant risk to the baby."
                },
                {
                    "pregnancy": "LTK-H Tablet is unsafe to use during pregnancy.<br>There is positive evidence of human fetal risk, but the benefits from use in pregnant women may be acceptable despite the risk, for example in life-threatening situations. Please consult your doctor."
                }
            ]
        },
        {
            "content": "",
            "how_medicine_works": "",
            "how_to_use": "",
            "id": "z5s5a+e/Cj4ip7sUl2zJFQ==",
            "medicine_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
            "is_rx_required": 0,
            "dosage_type": "",
            "medicine_name": "Mamy Poko Pants Extra Absorb NB1 - 20 Piece",
            "mrp": 195,
            "packing_size": "1 Packet of 20 Piece",
            "size": 1,
            "manufacturer_name": "Unicharm India",
            "side_effects": "",
            "medicine_category": "generic",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no",
            "warning_details": [
                {
                    "liver": ""
                },
                {
                    "alcohol": ""
                },
                {
                    "driving": ""
                },
                {
                    "kidney": ""
                },
                {
                    "lactation": ""
                },
                {
                    "pregnancy": ""
                }
            ]
        }
    ]
}
```
{% endtab %}
{% endtabs %}
