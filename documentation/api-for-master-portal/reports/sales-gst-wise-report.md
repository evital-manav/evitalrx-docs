---
description: To view Sales GST wise.
---

# Sales GST-wise Report

## Sales Report&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/master/reports/sales_purchase`

#### Request Body

| Name                                          | Type   | Description                                                                                                                                                                                                                                    |
| --------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| start\_date<mark style="color:red;">\*</mark> | String | <p>Start Date of the report. Must be less than equals to current Date or End Date.</p><p></p><p>Format = YYYY-MM-DD</p>                                                                                                                        |
| end\_date<mark style="color:red;">\*</mark>   | String | <p>End Date of the report. Must be greater than equals to Start Date and less than equals to current Date.</p><p></p><p>Format = YYYY-MM-DD</p><p></p><p>The duration between End Date and Start Date must be less than equals to 31 days.</p> |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                                                                                                                           |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-02-07 18:22:09",
    "data": {
        "results": [
            {
                "order_id": "YYLlhMzyFQuczFnrW3BQcQ==",
                "patient_id": "iXTFeOd5KUkXVz31xrA1ag==",
                "order_number": "O0IW100IZI",
                "payment_date": "2023-02-03 10:32:00",
                "reference_number": 52,
                "bill_no": "52",
                "order_datetime": "2023-02-03 10:31:52",
                "patient_name": "Manav Banglore",
                "patient_code": "P000105",
                "mobile": "7043120037",
                "address_line1": "Jogupalya",
                "address_line2": "Halasuru",
                "city": "Bengaluru",
                "state": "Karnataka",
                "country": "India",
                "payment_status": 1,
                "cess": 0,
                "gst_details": [
                    {
                        "gst_percentage": 0,
                        "gross_amount": 0,
                        "discount": 0,
                        "base_price": 0,
                        "cgst": 0,
                        "sgst": 0,
                        "igst": 0,
                        "total": 0
                    },
                    {
                        "gst_percentage": 5,
                        "gross_amount": 0,
                        "discount": 0,
                        "base_price": 0,
                        "cgst": 0,
                        "sgst": 0,
                        "igst": 0,
                        "total": 0
                    },
                    {
                        "gst_percentage": 12,
                        "gross_amount": 0,
                        "discount": 0,
                        "base_price": 0,
                        "cgst": 0,
                        "sgst": 0,
                        "igst": 0,
                        "total": 0
                    },
                    {
                        "gross_amount": 23.5,
                        "discount": 0,
                        "base_price": 19.92,
                        "cgst": 1.79,
                        "sgst": 1.79,
                        "total": 23.5,
                        "gst_percentage": 18
                    },
                    {
                        "gst_percentage": 28,
                        "gross_amount": 0,
                        "discount": 0,
                        "base_price": 0,
                        "cgst": 0,
                        "sgst": 0,
                        "igst": 0,
                        "total": 0
                    }
                ]
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "end_date is required",
    "datetime": "2023-02-07 18:18:22",
    "data": null
}
```
{% endtab %}
{% endtabs %}
