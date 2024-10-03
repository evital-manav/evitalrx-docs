# Order Return Save

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/b2b/return/save`

#### Request Body

| Name                                                 | Type              | Description                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| bill\_date<mark style="color:red;">\*</mark>         | date              | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                                                                                                                                                                                                                                                                                         |
| buyer\_chemist\_id<mark style="color:red;">\*</mark> | String            | Id to uniquely identify the chemist for whom the order is placed                                                                                                                                                                                                                                                                                                                                                                          |
| payment\_status<mark style="color:red;">\*</mark>    | Number            | <p>To choose payment mode of the order.</p><p>1: CASH</p><p>2: CREDIT</p><p>3: UPI</p><p>4: CHEQUE</p><p>5: PAYTM</p><p>6: CC/DC</p><p>7: RTGS/NEFT</p>                                                                                                                                                                                                                                                                                   |
| items<mark style="color:red;">\*</mark>              | Stringified Array | <p>List of items with quantity (in pills).</p><p>All the params are required shown below.</p><p>Medicine Id and batch should have unique combination.</p><p><em>i.e.</em> [{"medicine_id":"TF7Wm49nceLV+NmoM6HJYw==","batch":"WER321","expiry":"2030-02-01","mrp":23.5,"price_to_retailer":15.85,"quantity":10,"free":0,"hf":0,"base_price":15.85,"discount_percentage":0,"scheme_amount":0,"gst_percentage":12,"cess_percentage":5}]</p> |
| apikey<mark style="color:red;">\*</mark>             | String            | Authentication token                                                                                                                                                                                                                                                                                                                                                                                                                      |
| bill\_no                                             | String            | The bill number should match the bill number from sales in order to create sales return bill                                                                                                                                                                                                                                                                                                                                              |
| remark                                               | String            | Note for the Prescription                                                                                                                                                                                                                                                                                                                                                                                                                 |
| delivery\_note                                       | String            | Delivery notes if any                                                                                                                                                                                                                                                                                                                                                                                                                     |
| doctor\_id                                           | String            | Doctor ID                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| wholesale\_order\_id                                 | Number            | The ID of the related wholesale order                                                                                                                                                                                                                                                                                                                                                                                                     |
|                                                      |                   |                                                                                                                                                                                                                                                                                                                                                                                                                                           |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Bill created successfully",
    "datetime": "2024-10-01 14:56:06",
    "data": {
        "chemist_wholesale_return_id": "f4Prpako4VmiRuhdUA8gYg=="
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "bill_date must be in [YYYY-MM-DD, YYYY-MM-D, YYYY-M-D, YYYY-M-DD] format",
    "datetime": "2024-10-01 15:07:27",
    "data": null
}
```
{% endtab %}
{% endtabs %}
