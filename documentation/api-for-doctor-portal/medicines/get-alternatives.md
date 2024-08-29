---
description: To get Medicine alternatives on the basis of the drug composition
---

# Get Alternatives



## Get Alternatives

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/get_alternatives`

The API gives alternatives available of the Product.

#### Request Body

| Name                                           | Type   | Description                             |
| ---------------------------------------------- | ------ | --------------------------------------- |
| apikey<mark style="color:red;">\*</mark>       | String | Authentication Token                    |
| medicine\_id<mark style="color:red;">\*</mark> | String | Unique id of the product                |
| content<mark style="color:red;">\*</mark>      | String | Content/Drug of the medicine\_id passed |

{% tabs %}
{% tab title="200: OK Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-07 11:17:37",
    "data": [
        {
            "dosage_type": "tablet",
            "medicine_name": "Coldmark Tablet",
            "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
            "mrp": "45",
            "medicine_id": "q+td7wYsWZpHq87j7r8mbQ==",
            "packing_size": "1 Strip of  10 Tablet",
            "size": "10",
            "manufacturer_name": "Aerozest Life Science",
            "medicine_type": "drug",
            "gst_percentage": "12",
            "available_for_patient": "yes",
            "discontinued": "no",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no"
        },
        {
            "dosage_type": "tablet",
            "medicine_name": "Koldstat Tablet",
            "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
            "mrp": "50",
            "medicine_id": "kQw3reT/EVJg77T2Od3SZQ==",
            "packing_size": "1 Strip of  10 Tablet",
            "size": "10",
            "manufacturer_name": "Astra Idl Limited",
            "medicine_type": "drug",
            "gst_percentage": "12",
            "available_for_patient": "yes",
            "discontinued": "no",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no"
        },
        {
            "dosage_type": "tablet",
            "medicine_name": "Ultracold Tablet",
            "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
            "mrp": "50",
            "medicine_id": "zs1OJIrjjpi4l8t1WAXJmg==",
            "packing_size": "1 Strip of  10 Tablet",
            "size": "10",
            "manufacturer_name": "SPL Healthcare India Pvt. Ltd",
            "medicine_type": "drug",
            "gst_percentage": "12",
            "available_for_patient": "yes",
            "discontinued": "no",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no"
        },
        {
            "dosage_type": "tablet",
            "medicine_name": "Power 999 Tablet",
            "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
            "mrp": "35",
            "medicine_id": "5wpJHqB9SMuJq/wSbEaqmA==",
            "packing_size": "1 Strip of  10 Tablet",
            "size": "10",
            "manufacturer_name": "Medico Labs",
            "medicine_type": "drug",
            "gst_percentage": "12",
            "available_for_patient": "yes",
            "discontinued": "no",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no"
        },
        {
            "dosage_type": "tablet",
            "medicine_name": "Dpc Plus Tablet",
            "content": "Paracetamol (500mg) + Phenylephrine Hydrochloride (5mg) + Chlorpheniramine Maleate (2mg)",
            "mrp": "28.59",
            "medicine_id": "45ZNMjRkR0YRpo6zUdnEdw==",
            "packing_size": "1 Strip of  10 Tablet",
            "size": "10",
            "manufacturer_name": "Sunij Pharma Pvt Ltd",
            "medicine_type": "drug",
            "gst_percentage": "12",
            "available_for_patient": "yes",
            "discontinued": "no",
            "loose_quantity": 0,
            "sale_discount": 0,
            "strip_quantity": 0,
            "is_inventory_available": "no"
        }
    ]
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"Medicine Code\" is required",
    "datetime": "2022-12-07 11:19:46",
    "data": null
}
```
{% endtab %}
{% endtabs %}
