# Order Save as Draft

## Place Order

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in//v1/b2b/save_as_draft`&#x20;

#### Request Body

| Name                                                 | Type              | Description                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| bill\_date<mark style="color:red;">\*</mark>         | date              | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                                                                                                                                                                                                                                                                                         |
| buyer\_chemist\_id<mark style="color:red;">\*</mark> | String            | Id to uniquely identify the chemist for whom the order is placed                                                                                                                                                                                                                                                                                                                                                                          |
| items<mark style="color:red;">\*</mark>              | Stringified Array | <p>List of items with quantity (in pills).</p><p>All the params are required shown below.</p><p>Medicine Id and batch should have unique combination.</p><p><em>i.e.</em> [{"medicine_id":"TF7Wm49nceLV+NmoM6HJYw==","batch":"WER321","expiry":"2030-02-01","mrp":23.5,"price_to_retailer":15.85,"quantity":10,"free":0,"hf":0,"base_price":15.85,"discount_percentage":0,"scheme_amount":0,"gst_percentage":12,"cess_percentage":5}]</p> |
| apikey<mark style="color:red;">\*</mark>             | String            | Authentication token                                                                                                                                                                                                                                                                                                                                                                                                                      |
| payment\_status<mark style="color:red;">\*</mark>    | Number            | <p>To choose payment mode of the order.</p><p>1: CASH</p><p>2: CREDIT</p><p>3: UPI</p><p>4: CHEQUE</p><p>5: PAYTM</p><p>6: CC/DC</p><p>7: RTGS/NEFT</p>                                                                                                                                                                                                                                                                                   |
| payment\_due\_date                                   | date              | <p>Date of the bill.</p><p>Format: YYYY-MM-DD<br>(Required but conditional i.e. if payment_status is 2 then)</p>                                                                                                                                                                                                                                                                                                                          |
| bill\_no                                             | String            | The bill number, can be empty, or if you have any specific bill to save                                                                                                                                                                                                                                                                                                                                                                   |
| wholesale\_draft\_id                                 | number            | <p>The ID of the wholesale draft<br>(If draft order is being saved)</p>                                                                                                                                                                                                                                                                                                                                                                   |
| bill\_base                                           | String            | <p>Base for billing, accepts:<br>1. mrp<br>2. ptr (default)</p>                                                                                                                                                                                                                                                                                                                                                                           |
| shipping                                             | String            | The cost of shipping if made                                                                                                                                                                                                                                                                                                                                                                                                              |
| remark                                               | String            | Note for the Prescription                                                                                                                                                                                                                                                                                                                                                                                                                 |
| delivery\_note                                       | String            | Delivery notes if any                                                                                                                                                                                                                                                                                                                                                                                                                     |
| doctor\_id                                           | String            | Doctor ID                                                                                                                                                                                                                                                                                                                                                                                                                                 |

{% tabs %}
{% tab title="200 Order Saved successfully." %}
<pre><code><strong>{
</strong>    "status_code": "1",
    "status_message": "Bill created successfully",
    "datetime": "2024-10-01 12:50:37",
    "data": {
        "chemist_order_id": "QlOCazEdBCkSk9qdEQF2qA=="
    }
}
</code></pre>
{% endtab %}

{% tab title="200: OK Order failed." %}
```json
{
    "status_code": "0",
    "status_message": "Something broken. Please try again later.",
    "datetime": "2024-10-01 12:51:23",
    "data": null
}
```
{% endtab %}
{% endtabs %}

