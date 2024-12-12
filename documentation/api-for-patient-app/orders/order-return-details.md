# Order Return Details

## View Sales Return bill with API

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}patient/orders/sales_return/view`](https://api.evitalrx.in/v1/patient/orders/sales_return/view)

This API will make a Sales Return bill. chemist no need to go to the eVitalRx portal to complete the Return bill.

#### Request Body

| Name                                                         | Type   | Description                                      |
| ------------------------------------------------------------ | ------ | ------------------------------------------------ |
| <mark style="color:red;">\*</mark>chemist\_sales\_return\_id | String | Order ID from the Response of sales\_return API. |
| apikey<mark style="color:red;">\*</mark>                     | String | Authentication token                             |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-12-06 11:20:56",
    "ng_version": "0.0.787",
    "data": {
        "order_id": "zD2GbRYPHMaC/CL7Ot4Yjg==",
        "patient_name": "Avi Patel",
        "patient_id": "",
        "order_number": "EBD70731003365",
        "order_date": "2024-07-24",
        "amount": 23.5,
        "mobile": "",
        "order_status": "completed",
        "address": null,
        "address_line2": null,
        "city": null,
        "zipcode": null,
        "created_date": "2024-12-06 11:02:32",
        "total": 24,
        "payment_status": 2,
        "payment_date": "1900-01-01 12:00:00",
        "method_name": "Credit",
        "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
        "order_by_entity": "chemist",
        "reference_number": 4,
        "remark": "",
        "roundoff": 0.5,
        "utm_source": "",
        "doctor_id": "",
        "total_discount": 0,
        "lock_bill": "no",
        "user_id": 0,
        "parent_patient_id": "",
        "sales_reference_id": "",
        "is_unlink_record": "no",
        "total_gst": 2.41,
        "total_cess": 1,
        "total_qty": 10,
        "items": [
            {
                "medicine_id": "TF7Wm49nceLV+NmoM6HJYw==",
                "base_price": 23.5,
                "quantity": 10,
                "mrp": 23.5,
                "discount_percentage": 0,
                "batch": "WER321",
                "expiry": "2030-02-01",
                "gst": 2.41,
                "gst_percentage": 12,
                "cess": 1,
                "cess_percentage": 5,
                "hsn_code": "345335",
                "amount": 23.5,
                "medicine_name": "Ltk 50 Tablet",
                "size": 10,
                "pack_size": "10 Tablets",
                "packing_size": "10 tablets in 1 strip",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "content": "Losartan (50mg)",
                "location": "", // location of the medicine in pharmacy
                "stock_adjusted": "pending",
                "discount": 0,
                "order_type": "sale_return",
                "landing_price": 18.540045125038404
            }
        ],
        "billing_for_details": {
            "patient_id": "",
            "patient_name": "Avi Patel",
            "mobile": "",
            "aadhar_number": "",
            "patient_address": "",
            "patient_city": null,
            "gstn_number": "",
            "patient_zipcode": null,
            "profile_picture": "",
            "discount_percentage": 0,
            "email": "",
            "status": "active"
        },
        "is_already_adjusted": "no",
        "doctor_name": "",
        "customer_details": {
            "patient_id": "",
            "patient_name": "Avi Patel",
            "mobile": "",
            "aadhar_number": "",
            "patient_address": "",
            "patient_city": null,
            "gstn_number": "",
            "patient_zipcode": null,
            "profile_picture": "",
            "discount_percentage": 0,
            "email": "",
            "status": "active"
        },
        "chemist_details": {
            "id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
            "pharmacy_name": "Demo Pharmacy",
            "mobile": "8128937197",
            "pharmacist_digital_signature": "",
            "pharmacy_logo": "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/noixjea3n4.jpg",
            "profile_picture": "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/ic0qtzyda7.jpg"
        }
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "chemist_sales_return_id must be greater than 0",
    "datetime": "2024-12-06 11:24:24",
    "ng_version": "0.0.787",
    "data": null
}
```
{% endtab %}
{% endtabs %}
