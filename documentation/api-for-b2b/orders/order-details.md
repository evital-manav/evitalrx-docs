# Order Details

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}b2b/view`](https://api.evitalrx.in/v1/b2b/view)

#### Request Body

| Name                                                     | Type   | Description                                                             |
| -------------------------------------------------------- | ------ | ----------------------------------------------------------------------- |
| chemist\_wholesale\_id<mark style="color:red;">\*</mark> | String | Id to uniquely identify the chemist for whom the details has been asked |
| apikey<mark style="color:red;">\*</mark>                 | String | Authentication token                                                    |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 13:43:43",
    "data": {
        "wholesale_id": "SZ6AfI2e+h+Kb18NnvBDMA==", // Order ID
        "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
        "owner_pharmacy_name": "Demo Pharmacy",
        "owner_mobile": "8128937197",
        "owner_email": "khush.shah@evital.in",
        "owner_gstn_number": "05AAABB0639G1Z8",
        "owner_address": "4d Square Mall",
        "owner_address_line2": "Opp. Mr. Diy",
        "owner_area": "Motera",
        "owner_city": "Ahmedabad",
        "owner_state": "Gujarat",
        "owner_zipcode": "380005",
        "buyer_chemist_id": "bOhA95wWipFevGWyHpujmg==",
        "buyer_pharmacy_name": "Test Pharma",
        "buyer_mobile": "7878989877",
        "buyer_email": "",
        "buyer_gstn_number": "",
        "buyer_address": "",
        "buyer_address_line2": "",
        "buyer_area": "",
        "buyer_city": "Ahmedabad",
        "buyer_state": "Gujarat",
        "buyer_zipcode": "380013",
        "bill_date": "2024-09-23",
        "bill_no": "11",
        "order_number": "7247878068",
        "amount": 1338,
        "due_amount": 1338,
        "buyer_pan_no": "",
        "created_date": "2024-09-23 16:15:28",
        "order_status": "completed",
        "payment_status": 2,
        "payment_date": "2024-09-23 16:15:28",
        "payment_due_date": "2024-09-29",
        "margin": 459.94,
        "roundoff": 0.46,
        "einvoice_url": "",
        "einvoice_qr": "",
        "einvoice_irn": "",
        "shipping": 0,
        "tds_percentage": 0,
        "tds": 0,
        "tcs_percentage": 0,
        "tcs": 0,
        "bill_base": "ptr",
        "remark": "",
        "reference_number": 11,
        "payment_ref_id": "",
        "eway_billno": "",
        "eway": {},
        "delivery_note": "",
        "doctor_id": "LxH7UjhNHdXQY4F8MC4wBA==",
        "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
        "order_by_entity": "chemist",
        "method_name": "Credit",
        "buyer_latitude": "0",
        "buyer_longitude": "0",
        "delivery_id": "",
        "buyer_license_number_20": "",
        "buyer_license_number_21": "",
        "total": 1338,
        "total_qty": 80,
        "total_discount": 0,
        "total_items": 1,
        "total_gst": 137.18,
        "total_cess": 57.16,
        "items": [
            {
                "id": "LyGWvI0Ah0CCoZzgO8HAdw==",
                "chemist_wholesale_id": "SZ6AfI2e+h+Kb18NnvBDMA==",
                "medicine_id": "TF7Wm49nceLV+NmoM6HJYw==", // Medicine ID
                "batch": "ADASASD",
                "expiry": "2029-02-01",
                "mrp": 23.5,
                "quantity": 80,
                "free": 0,
                "price_to_retailer": 14.29,
                "discount_percentage": 0,
                "discount": 0,
                "base_price": 14.29,
                "gst_percentage": 12,
                "gst": 1.7148,
                "amount": 1337.54,
                "size": 10,
                "scheme_amount": 0,
                "margin_percentage": 0,
                "cess": 0.7145,
                "cess_percentage": 5,
                "hsn_code": "",
                "medicine_name": "Ltk 50 Tablet",
                "schedule_type": "H1",
                "pack_size": "10 Tablets",
                "packing_size": "10 tablets in 1 strip",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "landing_price": 16.449848300677342,
                "location": "", // Location where the Product was placed in pharmacy
                "sale_b2b_discount": 0,
                "taxable": 1143.2
            }
        ],
        "seller_chemist_details": {
            "profileData": {
                "gstn_number": "05AAABB0639G1Z8",
                "email": "khush.shah@evital.in",
                "mobile": "8128937197",
                "city": "Ahmedabad",
                "pharmacy_name": "Demo Pharmacy",
                "address": "4d Square Mall",
                "address_line2": "Opp. Mr. Diy",
                "pharmacy_logo": "",
                "chemist_qrcode_link": "localhost/evital/code/QCTPOAX/",
                "license_number_20": "EFCS4645156",
                "license_number_21": "EFCS4645151",
                "fssai": "12345678910112",
                "license_20b": "RFVGRF",
                "license_21b": "123456Y7892",
                "license_20f": "5943094438943",
                "fssai_number": "12345678910112"
            },
            "shopTimings": {
                "fullday_working": "",
                "timings": {}
            },
        },
        "doctor_name": "Aagam Jain",
        "doctor_address": "",
        "doctor_area": "",
        "doctor_city": "ahmedabad",
        "doctor_state": "gujarat",
        "doctor_zipcode": "",
        "doctor_license": "JDLKSJ439398"
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "chemist_wholesale_id is required",
    "datetime": "2024-10-01 13:44:04",
    "data": null
}
```
{% endtab %}
{% endtabs %}
