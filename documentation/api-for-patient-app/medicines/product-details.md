---
description: To get item details in your inventory by unique medicine Id.
---

# Product Details

## Product Details

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/medicines/view`

#### Request Body

| Name                                           | Type    | Description                                                                                                                                                                                                                                                                                                     |
| ---------------------------------------------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String  | Authentication Token                                                                                                                                                                                                                                                                                            |
| medicine\_id<mark style="color:red;">\*</mark> | String  | Unique id of the product                                                                                                                                                                                                                                                                                        |
| medicine\_ids                                  | String  | <p>Stringified Array of medicine_ids.</p><p></p><p><strong>medicine_id</strong> param is optional, if <strong>medicine_ids</strong> param is passed.</p><p></p><p>medicine_ids should contain at least 2 medicine_ids.</p><p></p><p>Example:</p><p>["z5s5a+e/Cj4ip7sUl2zJFQ==", "otUfMtG4nIpWSc+oWoX7Lw=="]</p> |
| show\_sale\_rate                               | yes\|no | <p>To show the medicines on discounted rate. </p><p></p><p>yes | price = mrp - discount</p><p></p><p>no | price = mrp</p><p></p><p>Default: no</p>                                                                                                                                                              |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-03-09 19:01:02",
    "data": [
        {
            "content": "Losartan (50mg)",
            "how_medicine_works": "Ltk 50 Tablet is an angiotensin receptor blocker (ARB). It relaxes blood vessel by blocking the action of a chemical that usually makes blood vessels tighter. This lowers the blood pressure, allowing the blood to flow more smoothly to different organs and the heart to pump more efficiently.",
            "how_to_use": "Take this medicine in the dose and duration as advised by your doctor. Swallow it as a whole. Do not chew, crush or break it. Ltk 50 Tablet may be taken with or without food, but it is better to take it at a fixed time.",
            "id": "y8P5ElKQqfn/Dkb0uhE9Sg==",
            "medicine_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
            "is_rx_required": 0,
            "dosage_type": "tablet",
            "medicine_name": "Ltk 50 Tablet",
            "mrp": 23.5,
            "packing_size": "1 Strip of  10 Tablet",
            "pack_size": "10 Tablet",
            "packing": "Strip",
            "size": 10,
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "side_effects": " Common   Dizziness  Back pain  Sinus inflammation  Increased potassium level in blood  ",
            "medicine_category": "drug",
            "loose_quantity": 1022,
            "sale_discount": 15,
            "strip_quantity": 102,
            "is_inventory_available": "yes",
            "price": 23.5,
            "sell_in_loose": "yes",
            "warning_details": [
                {
                    "liver": "Ltk 50 Tablet should be used with caution in patients with liver disease. Dose adjustment of Ltk 50 Tablet may be needed. Please consult your doctor.<br>Use of Ltk 50 Tablet is not recommended in patients with severe liver disease."
                },
                {
                    "alcohol": "Taking Losartan with alcohol may excessively lower the blood pressure."
                },
                {
                    "driving": "It is not known whether Ltk 50 Tablet alters the ability to drive. Do not drive if you experience any symptoms that affect your ability to concentrate and react."
                },
                {
                    "kidney": "Ltk 50 Tablet is safe to use in patients with kidney disease. No dose adjustment of Ltk 50 Tablet is recommended.<br>However, talk to your doctor if you have any underlying kidney disease. Regular monitoring of blood pressure is recommended for better dose adjustment."
                },
                {
                    "lactation": "Ltk 50 Tablet is probably safe to use during lactation.  Limited human data suggests that the drug does not represent a significant risk to the baby."
                },
                {
                    "pregnancy": "Ltk 50 Tablet is unsafe to use during pregnancy.<br>There is positive evidence of human fetal risk, but the benefits from use in pregnant women may be acceptable despite the risk, for example in life-threatening situations. Please consult your doctor."
                }
            ],
            "salt_content_id": "KOKzk7o+BiY7KaYIIL5JDg=="
        }
    ]
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
    "datetime": "2023-03-09 19:02:40",
    "data": [
        {
            "content": "Hydrochlorothiazide (12.5mg) + Losartan (50mg)",
            "how_medicine_works": "LTK-H Tablet is a combination of two medicines: Losartan and Hydrochlorothiazide, which lowers the blood pressure effectively. Losartan is an angiotensin receptor blocker (ARB). It works by blocking the hormone angiotensin thereby relaxing blood vessels. This allows the blood to flow more smoothly and the heart to pump more efficiently. Hydrochlorothiazide is a diuretic that removes extra water and certain electrolytes from the body. Over time it also relaxes blood vessels and improves blood flow.",
            "how_to_use": "Take this medicine in the dose and duration as advised by your doctor. Swallow it as a whole. Do not chew, crush or break it. LTK-H Tablet may be taken with or without food, but it is better to take it at a fixed time.",
            "id": "vjalpzMV0E33BLwzzLR6fQ==",
            "medicine_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
            "is_rx_required": 1,
            "dosage_type": "tablet",
            "medicine_name": "LTK-H Tablet",
            "mrp": 36.1,
            "packing_size": "1 Strip of  10 Tablet",
            "pack_size": "10 Tablet",
            "packing": "Strip",
            "size": 10,
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "side_effects": " Common   Nausea  Taste change  Stomach upset  Diarrhea  Headache  Dizziness  Weakness  Decreased blood pressure  Increased blood uric acid  Increased blood lipid level  Glucose intolerance  Electrolyte imbalance  ",
            "medicine_category": "drug",
            "loose_quantity": 344,
            "sale_discount": 0,
            "strip_quantity": 34,
            "is_inventory_available": "yes",
            "price": 36.1,
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
            ],
            "salt_content_id": "KOKzk7o+BiY7KaYIIL5JDg=="
        },
        {
            "content": "Losartan (50mg)",
            "how_medicine_works": "Ltk 50 Tablet is an angiotensin receptor blocker (ARB). It relaxes blood vessel by blocking the action of a chemical that usually makes blood vessels tighter. This lowers the blood pressure, allowing the blood to flow more smoothly to different organs and the heart to pump more efficiently.",
            "how_to_use": "Take this medicine in the dose and duration as advised by your doctor. Swallow it as a whole. Do not chew, crush or break it. Ltk 50 Tablet may be taken with or without food, but it is better to take it at a fixed time.",
            "id": "y8P5ElKQqfn/Dkb0uhE9Sg==",
            "medicine_image": "https://d1tu4pmhr82np8.cloudfront.net/storage/medicines/default.jpg",
            "is_rx_required": 0,
            "dosage_type": "tablet",
            "medicine_name": "Ltk 50 Tablet",
            "mrp": 23.5,
            "packing_size": "1 Strip of  10 Tablet",
            "pack_size": "10 Tablet",
            "packing": "Strip",
            "size": 10,
            "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
            "side_effects": " Common   Dizziness  Back pain  Sinus inflammation  Increased potassium level in blood  ",
            "medicine_category": "drug",
            "loose_quantity": 1022,
            "sale_discount": 15,
            "strip_quantity": 102,
            "is_inventory_available": "yes",
            "price": 23.5,
            "sell_in_loose": "yes",
            "warning_details": [
                {
                    "liver": "Ltk 50 Tablet should be used with caution in patients with liver disease. Dose adjustment of Ltk 50 Tablet may be needed. Please consult your doctor.<br>Use of Ltk 50 Tablet is not recommended in patients with severe liver disease."
                },
                {
                    "alcohol": "Taking Losartan with alcohol may excessively lower the blood pressure."
                },
                {
                    "driving": "It is not known whether Ltk 50 Tablet alters the ability to drive. Do not drive if you experience any symptoms that affect your ability to concentrate and react."
                },
                {
                    "kidney": "Ltk 50 Tablet is safe to use in patients with kidney disease. No dose adjustment of Ltk 50 Tablet is recommended.<br>However, talk to your doctor if you have any underlying kidney disease. Regular monitoring of blood pressure is recommended for better dose adjustment."
                },
                {
                    "lactation": "Ltk 50 Tablet is probably safe to use during lactation.  Limited human data suggests that the drug does not represent a significant risk to the baby."
                },
                {
                    "pregnancy": "Ltk 50 Tablet is unsafe to use during pregnancy.<br>There is positive evidence of human fetal risk, but the benefits from use in pregnant women may be acceptable despite the risk, for example in life-threatening situations. Please consult your doctor."
                }
            ],
            "salt_content_id": "KOKzk7o+BiY7KaYIIL5JDg=="
        }
    ]
}
```
{% endtab %}
{% endtabs %}
