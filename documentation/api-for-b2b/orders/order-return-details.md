# Order Return Details

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}b2b/return/view`](https://api.evitalrx.in/v1/b2b/return/view)

#### Request Body

| Name                                                             | Type   | Description                                                             |
| ---------------------------------------------------------------- | ------ | ----------------------------------------------------------------------- |
| chemist\_wholesale\_return\_id<mark style="color:red;">\*</mark> | String | Id to uniquely identify the chemist for whom the details has been asked |
| apikey<mark style="color:red;">\*</mark>                         | String | Authentication token                                                    |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "",
    "datetime": "2024-10-01 15:32:00",
    "data": {
        "wholesale_return_id": "2kz3qQobevj9wkrgNXyPHQ==", // Return Order ID
        "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
        "reference_number": 6,
        "owner_pharmacy_name": "Demo Pharmacy",
        "owner_mobile": "8128937197",
        "owner_email": "khush.shah@evital.in",
        "owner_gstn_number": "05AAABB0639G1Z8",
        "owner_address": "4d Square Mall",
        "owner_address_line2": "Opp. Mr. Diy",
        "owner_city": "Ahmedabad",
        "owner_state": "Gujarat",
        "owner_zipcode": "380005",
        "buyer_chemist_id": "bOhA95wWipFevGWyHpujmg==",
        "buyer_pharmacy_name": "Test Pharma",
        "buyer_mobile": "7878989877",
        "buyer_gstn_number": "",
        "buyer_address": "",
        "buyer_address_line2": "",
        "buyer_area": "",
        "buyer_city": "Ahmedabad",
        "buyer_state": "Gujarat",
        "buyer_zipcode": "380013",
        "bill_date": "2024-09-23",
        "bill_no": "",
        "order_number": "0547754682",
        "order_status": "completed",
        "amount": 1338,
        "delivery_note": "",
        "created_date": "2024-09-24 16:54:05",
        "payment_status": 2,
        "payment_date": "2024-09-24 16:54:05",
        "roundoff": 0.46,
        "einvoice_irn": "",
        "einvoice_qr": "",
        "einvoice_url": "",
        "doctor_id": "LxH7UjhNHdXQY4F8MC4wBA==",
        "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
        "order_by_entity": "chemist",
        "wholesale_reference_id": "oC8H6iM43tYvLhzpmVxaMw==",
        "buyer_pharmacy_status": "active",
        "buyer_license_number_20": "",
        "buyer_license_number_21": "",
        "total": 1338,
        "total_qty": 80,
        "total_items": 1,
        "total_gst": 137.18,
        "total_cess": 57.16,
        "items": [
            {
                "id": "mPaPfB/3j9xS45qABp+07A==",
                "chemist_wholesale_return_id": "2kz3qQobevj9wkrgNXyPHQ==",
                "medicine_id": "TF7Wm49nceLV+NmoM6HJYw==",
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
                "cess": 0.7145,
                "cess_percentage": 5,
                "hsn_code": "",
                "medicine_name": "Ltk 50 Tablet",
                "pack_size": "10 Tablets",
                "packing_size": "10 tablets in 1 strip",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "landing_price": 16.449848300677342,
                "location": "",
                "taxable": 1143.2
            }
        ],
        "total_discount": 0,
        "settingResults": {
            "terms_and_conditions_wholesale": ""
        },
        "staff_list": [
            {
                "id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "fullname": "Owner",
                "status": "active",
                "entity": "chemist",
                "role_id": "aBs1Hvl3Duj0n3tGG09Biw=="
            },
            {
                "id": "AUggj/Nbe8fOBBWEUBAysA==",
                "firstname": "Raju",
                "lastname": "R",
                "status": "active",
                "role_id": "S7BTDcQD0IFOO7ypLxnmRg==",
                "role_name": "Store Manager",
                "fullname": "Raju R",
                "entity": "staff"
            }
        ],
        "doctor_name": "Aagam Jain",
        "is_already_adjusted": "no",
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
    "status_message": "Invalid Chemist Wholesale Return ID",
    "datetime": "2024-10-01 15:33:17",
    "data": null
}
```
{% endtab %}
{% endtabs %}
