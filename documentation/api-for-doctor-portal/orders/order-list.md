---
description: To get the order details
---

# Order List

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}doctor/orders/list`](https://api.evitalrx.in/v1/doctor/orders/list)

#### Request Body

| Name                                          | Type   | Description                              |
| --------------------------------------------- | ------ | ---------------------------------------- |
| start\_date<mark style="color:red;">\*</mark> | String | Start date of orders.                    |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                     |
| end\_date<mark style="color:red;">\*</mark>   | String | End date of orders.                      |
| page                                          | Number | For pagination purpose. default: 1       |
| patient\_id<mark style="color:red;">\*</mark> | String | ID of the patient you want to see orders |
| remark                                        | String | To search orders with notes              |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-06 10:47:27",
    "data": {
        "results": [
            {
                "id": "X+j2u3xGNvyTzLrZCz+g+Q==", // Order ID
                "bill_no": "",
                "order_number": "OMLN8WCXGU",
                "order_delivery_datetime": "2023-10-02 18:28:38",
                "delivery_type": "delivery",
                "order_status": "draft",
                "created_date": "2023-10-02 18:28:38",
                "amount": 4870,
                "remark": "ICU Patient" // remarks from patient/other entity
            }
        ],
        "rpp": 20,
        "current_page": 1
    }
}
```
{% endtab %}

{% tab title="200: OK No Record found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-09-13 15:03:43",
    "data": {
        "results": [],
        "rpp": 20,
        "current_page": 1
    }
}
```
{% endtab %}

{% tab title="200: OK Error" %}


```json
{
    "status_code": "0",
    "status_message": "patient_id is required",
    "datetime": "2023-09-13 15:04:00",
    "data": null
}
```
{% endtab %}
{% endtabs %}

