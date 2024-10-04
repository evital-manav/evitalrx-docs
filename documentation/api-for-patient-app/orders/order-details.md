---
description: To get the order details
---

# Order Details

## Order View

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/orders/view`

#### Request Body

| Name                                        | Type   | Description            |
| ------------------------------------------- | ------ | ---------------------- |
| order\_id<mark style="color:red;">\*</mark> | String | Unique id of the Order |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token   |

{% tabs %}
{% tab title="200 Order successfully retrieved." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 19:09:07",
    "data": {
        "id": "/6vMKQj0JOB9GvN+6I27zg==",
        "order_number": "OJLBC8WC1I",
        "amount": 10000,
        "discount": 0,
        "total": 10000,
        "address_name": "home",
        "address": "Cambridge Road, Halasuru",
        "address_line2": "",
        "city": "Banglore",
        "state": "Karnataka",
        "zipcode": "560008",
        "order_status": "assigned",
        "created_date": "2022-12-06 18:46:30",
        "order_delivery_datetime": "2022-12-06 18:46:30",
        "pharmacy_name": "Manav Pharmacy",
        "chemist_mobile": "7043120038",
        "chemist_address": "Cambridge Road",
        "chemist_city": "Bengaluru",
        "chemist_latitude": 12.970622,
        "chemist_longitude": 77.6281433,
        "chemist_state": "Karnataka",
        "chemist_zipcode": "560008",
        "order_patient_name": "Jay Patel",
        "pharmacist_name": "Manav",
        "delivery_note": "",
        "payment_status": 2,
        "patient_id": "KFb7duiHDJAXqKUJc2poVw==",
        "delivery_pin": "U2FsdGVkX1/ChV2gPONI9ava2S0tZ8h9Hf7LAV2E6WA=",
        "payment_ref_id": "",
        "custom_fields": [
            {
                "id": "Ld8/i0ldfhC/rab1KHw5vA==",
                "attribute_key": "test1",
                "attribute_value": "123"
            },
            {
                "id": "1G0LbvVlHLTYUZLiGgU5gA==",
                "attribute_key": "test2",
                "attribute_value": "12"
            }
        ],
        "medicine_details": [
            {
                "medicine_id": "Eli4pMFfzobV63G67jtjZw==",
                "medicine_name": "Ltk AM Tablet 569",
                "size": 10,
                "medicine_type": "drug",
                "packing_size": "1 Strip of  10 Tablet",
                "gst_percentage": 12,
                "quantity": 10,
                "mrp": 1000,
                "amount": 10000,
                "price": 1000,
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "order_details_id": "ai79ZnBDqmAibtajMJfCcQ==",
                "discount_percentage": 0,
                "batch": "",
                "discount": 0,
                "expiry": "1900-01-01",
                "gst": 0,
                "hsn_code": "",
                "cess": 0,
                "cess_percentage": 0,
                "loose_quantity": 100
            }
        ],
        "prescription_details": [],
        "payment_url": "http://evital.in/invoice/T0pMQkM4V0MxSQ==/"
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Order Key",
    "datetime": "2022-12-06 18:57:35",
    "data": null
}
```
{% endtab %}
{% endtabs %}

