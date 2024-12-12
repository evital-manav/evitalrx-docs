# Order Return List

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}b2b/return/list`](https://api.evitalrx.in/v1/b2b/return/list)

#### Request Body

| Name                                          | Type   | Description                                                                                                                                                              |
| --------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| start\_date<mark style="color:red;">\*</mark> | Date   | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                        |
| end\_date<mark style="color:red;">\*</mark>   | Date   | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                        |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                                                     |
| order\_number                                 | String | Unique order number which got generated while saving order                                                                                                               |
| bill\_no                                      | String | The number of the bill like for eg. 1, 2, 3...                                                                                                                           |
| reference\_number                             | Number | Generated reference number to bill for eg. 1, 2, 3...                                                                                                                    |
| buyer\_chemist\_id                            | String | Id to uniquely identify the chemist for whom the order is saved                                                                                                          |
| searchstring                                  | String | <p>Min: 3 char required, accepts:<br>1. pharmacy_name<br>2. area</p>                                                                                                     |
| payment\_status                               | Number | <p>To choose payment mode of the order.</p><p>1: CASH</p><p>2: CREDIT</p><p>3: UPI</p><p>4: CHEQUE</p><p>5: PAYTM</p><p>6: CC/DC</p><p>7: RTGS/NEFT</p>                  |
| orderby                                       | String | <p>Field to order results by, accepts:<br>1. reference_number<br>2. bill_no<br>3. bill_date<br>4. created_date (default)<br>5. pharmacy_name<br>6. amount<br>7. area</p> |
| order                                         | String | <p>Order direction, accepts:<br>1. asc<br>2. desc (default)</p>                                                                                                          |
| remark                                        | String | Note for the Prescription if any                                                                                                                                         |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 15:27:42",
    "data": {
        "rpp": 20,
        "current_page": 1,
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
        "results": [
            {
                "id": "tktJBTVofF3vGazDa6GlOQ==", // Rturn Order ID
                "buyer_chemist_id": "9RraDPXEXeI+7FJlRkv7Kw==",
                "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "area": "",
                "reference_number": 58,
                "bill_no": "",
                "bill_date": "2024-09-24",
                "amount": 847,
                "payment_status": 2,
                "order_number": "0340854368",
                "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "order_by_entity": "chemist",
                "order_by_name": "Owner",
                "created_date": "2024-10-01 15:07:08",
                "remark": "",
                "pharmacy_name": "rrr",
                "einvoice_url": "",
                "mobile": "7656789034",
                "total": 0
            },
            {
                "id": "f4Prpako4VmiRuhdUA8gYg==",
                "buyer_chemist_id": "9RraDPXEXeI+7FJlRkv7Kw==",
                "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "area": "",
                "reference_number": 57,
                "bill_no": "",
                "bill_date": "2024-09-24",
                "amount": 847,
                "payment_status": 2,
                "order_number": "3983669004",
                "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "order_by_entity": "chemist",
                "order_by_name": "Owner",
                "created_date": "2024-10-01 14:56:06",
                "remark": "",
                "pharmacy_name": "rrr",
                "einvoice_url": "",
                "mobile": "7656789034",
                "total": 0
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
    "status_message": "start_date is required",
    "datetime": "2024-10-01 15:28:28",
    "data": null
}
```
{% endtab %}
{% endtabs %}
