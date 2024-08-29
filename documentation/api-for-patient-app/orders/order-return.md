# Order Return

## Make Sales Return bill with API

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in//v1/patient/orders/sales_return`

This API will make a Sales Return bill. chemist no need to go to the eVitalRx portal to complete the Return bill.

#### Request Body

| Name                                              | Type              | Description                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark>     | String            | Id to uniquely identify the patient for whom the order is placed                                                                                                                                                                                                                                                                                                                |
| items<mark style="color:red;">\*</mark>           | Stringified Array | <p>List of items with quantity (in pills). </p><p>All  the params are required shown below. </p><p>Medicine Id and batch should have unique combination. </p><p></p><p><em>i.e.</em> [{ "medicine_id": "vjalpzMV0E33BLwzzLR6fQ==", "batch": "FRESH", "expiry": "2025-12-01", "mrp": 36.1, "quantity": 2, "discount": 0, "gst_percentage": 12, "cess_percentage": 0}]</p><p></p> |
| apikey<mark style="color:red;">\*</mark>          | String            | Authentication token                                                                                                                                                                                                                                                                                                                                                            |
| patient\_name<mark style="color:red;">\*</mark>   | String            | Name of the Patient                                                                                                                                                                                                                                                                                                                                                             |
| remark                                            | String            | Note for the Order Return.                                                                                                                                                                                                                                                                                                                                                      |
| order\_date<mark style="color:red;">\*</mark>     | String            | <p>Date of the bill. </p><p>Format: YYYY-MM-DD</p><p></p>                                                                                                                                                                                                                                                                                                                       |
| payment\_status<mark style="color:red;">\*</mark> | Number            | <p>To choose payment mode of the order. </p><p>1: CASH </p><p>2: CREDIT </p><p>3: UPI </p><p>4: CHEQUE </p><p>5: PAYTM </p><p>6: CC/DC </p><p>7: RTGS/NEFT</p>                                                                                                                                                                                                                  |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Return order added successfully.",
    "datetime": "2023-03-09 18:44:25",
    "ng_version": "0.0.371",
    "data": {
        "order_id": "UpQGYF77Y97maydwXEaVXQ=="
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Patient Name length must be less than or equal to 50 characters long",
    "datetime": "2023-03-09 18:37:21",
    "data": null
}
```
{% endtab %}
{% endtabs %}
