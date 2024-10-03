---
description: To get the order details
---

# Order List

## Order List

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/b2b/list`

#### Request Body

| Name                                          | Type   | Description                                                                                                                                                                               |
| --------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| start\_date<mark style="color:red;">\*</mark> | Date   | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                                         |
| end\_date<mark style="color:red;">\*</mark>   | Date   | <p>Date of the bill.</p><p>Format: YYYY-MM-DD</p>                                                                                                                                         |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                                                                      |
| order\_number                                 | String | Unique order number which got generated while saving order                                                                                                                                |
| bill\_no                                      | String | The number of the bill like for eg. 1, 2, 3...                                                                                                                                            |
| reference\_number                             | Number | Generated reference number to bill (e.g. 1, 2, 3, ...)                                                                                                                                    |
| searchstring                                  | String | <p>Min: 3 char required, accepts:<br>1. pharmacy_name<br>2. area</p>                                                                                                                      |
| payment\_status                               | Number | <p>To choose payment mode of the order.</p><p>1: CASH</p><p>2: CREDIT</p><p>3: UPI</p><p>4: CHEQUE</p><p>5: PAYTM</p><p>6: CC/DC</p><p>7: RTGS/NEFT</p>                                   |
| buyer\_chemist\_id                            | String | Id to uniquely identify the chemist for whom the order is saved                                                                                                                           |
| orderby                                       | String | <p>Field to order results by, accepts:<br>1. reference_number<br>2. bill_no<br>3. bill_date<br>4. created_date (default)<br>5. pharmacy_name<br>6. amount<br>7. area<br>8. due_amount</p> |
| order                                         | String | <p>Order direction, accepts:<br>1. asc<br>2. desc (default)</p>                                                                                                                           |
| remark                                        | String | Note for the Prescription if any                                                                                                                                                          |



{% tabs %}
{% tab title="200: OK Order successfully retrieved." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 13:11:32",
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
                "id": "4opko4aPVaWqRvxgkS68gQ==",
                "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "buyer_chemist_id": "bOhA95wWipFevGWyHpujmg==",
                "reference_number": 104,
                "bill_no": "104",
                "bill_date": "2024-09-27",
                "amount": 1033,
                "payment_status": 2,
                "order_number": "5270311112",
                "delivery_note": "",
                "order_status": "completed",
                "order_type": "wholesale",
                "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "order_by_entity": "chemist",
                "order_by_name": "Owner",
                "created_date": "2024-10-01 12:54:23",
                "pharmacy_name": "Test Pharma",
                "mobile": "7878989877",
                "area": "",
                "einvoice_url": "",
                "payment_due_date": "2024-09-29",
                "total": 1033,
                "payment_cleared": "yes"
            },
            {
                "id": "QlOCazEdBCkSk9qdEQF2qA==",
                "chemist_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "buyer_chemist_id": "bOhA95wWipFevGWyHpujmg==",
                "reference_number": 103,
                "bill_no": "103",
                "bill_date": "2024-09-27",
                "amount": 1033,
                "payment_status": 2,
                "order_number": "0028515386",
                "delivery_note": "",
                "order_status": "completed",
                "order_type": "wholesale",
                "order_by_id": "pAUYuNJCJxZDFD5U4Nq/ZQ==",
                "order_by_entity": "chemist",
                "order_by_name": "Owner",
                "created_date": "2024-10-01 12:50:37",
                "pharmacy_name": "Test Pharma",
                "mobile": "7878989877",
                "area": "",
                "einvoice_url": "",
                "payment_due_date": "2024-09-29",
                "total": 1033,
                "payment_cleared": "yes"
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
    "status_message": "end_date must be greater than or equal to ref:start_date",
    "datetime": "2024-10-01 13:13:51",
    "data": null
}
```
{% endtab %}
{% endtabs %}
