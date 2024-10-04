---
description: To get the order details
---

# Order Details

## Order View

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/orders/view`

#### Request Body

| Name                                        | Type   | Description                                                            |
| ------------------------------------------- | ------ | ---------------------------------------------------------------------- |
| order\_id<mark style="color:red;">\*</mark> | String | Unique id of the order                                                 |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token                                                   |
| order\_number                               | String | if **order\_number** is provided, then **order\_id** is not mandatory. |

{% tabs %}
{% tab title="200: OK Order successfully retrieved." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-07 14:26:53",
    "data": {
        "id": "JoPUmfKRiivtIxpkAKtpng==",
        "order_number": "OOLBDETJIQ",
        "amount": 115,
        "discount": 0,
        "total": 115,
        "address_name": "home",
        "address": "",
        "address_line2": "",
        "city": "",
        "state": "",
        "zipcode": "",
        "order_status": "draft",
        "created_date": "2022-12-07 14:20:04",
        "order_delivery_datetime": "2022-12-07 14:20:04",
        "pharmacy_name": "Manav Pharmacy",
        "chemist_mobile": "7043120038",
        "chemist_address": "Cambridge Road",
        "chemist_city": "Bengaluru",
        "chemist_latitude": 12.970622,
        "chemist_longitude": 77.6281433,
        "chemist_state": "Karnataka",
        "chemist_zipcode": "560008",
        "order_patient_name": "Poojan Mehta",
        "pharmacist_name": "Manav",
        "delivery_note": "",
        "payment_status": 2,
        "patient_id": "3Dc6fhD+sruK/l2h585s7w==",
        "delivery_pin": "U2FsdGVkX1+twZ9Ase9xSlahDQno3tEh1A/fF3RGZI4=",
        "payment_ref_id": "",
        "custom_fields": {
                "prescription_id": "879",
                "appointment_id": "123"
            }
        "medicine_details": [
            {
                "medicine_id": "ZnsQl586DmR/ANT3aLdM4g==",
                "medicine_name": "Ltk 50 Tablet",
                "size": 10,
                "medicine_type": "drug",
                "packing_size": "10 tablets in 1 strip",
                "gst_percentage": 5,
                "quantity": 1,
                "mrp": 115,
                "amount": 0,
                "price": 0,
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "order_details_id": "XvpcrpsRCyGhtkVsFpFOeA==",
                "discount_percentage": 0,
                "batch": "KRI",
                "discount": 0,
                "expiry": "2023-02-01",
                "gst": 0,
                "hsn_code": "",
                "cess": 0,
                "cess_percentage": 0,
                "loose_quantity": 10
            }
        ],
        "prescription_details": [],
        "payment_url": "http://evital.in/invoice/T09MQkRFVEpJUQ==/"
    }
}
```
{% endtab %}

{% tab title="200: OK Could not find an order matching this query." %}
```json
{
    "status_code": "0",
    "status_message": "No record found",
    "datetime": "2022-12-07 14:30:56",
    "data": null
}
```
{% endtab %}
{% endtabs %}
