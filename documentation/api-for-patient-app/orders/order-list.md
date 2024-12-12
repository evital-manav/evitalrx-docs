---
description: To fetch order history of patient.
---

# Order List

## Order List

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/orders/list`](https://api.evitalrx.in/v1/patient/orders/list)

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id                              | String | Id to uniquely identify the Patient to fetch the list of orders of the particular patient                                                                                                                                                                                                                                                                        |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                                                                                                                                                                                                                                                             |
| page                                     | Number | To view orders on the next page. 20 Records will show at a time. The default page is 1.                                                                                                                                                                                                                                                                          |
| order\_mode                              | String | <p>'' | 'online' | 'offline'</p><p></p><p>Default: ''</p><p></p><p>If it is online, then only online orders will be fetched of the patients. </p><p></p><p>If provided offline, then only offline orders will be fetched from patients. </p><p></p><p>If not provided, or provided as '' then, it will fetch both online and offline orders of the patient. </p> |

{% tabs %}
{% tab title="200 Orders successfully retrieved." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-02-08 12:20:04",
    "data": {
        "results": [
            {
                "id": "bMLgI5pkJQJrKUqANIyVAA==",
                "bill_no": "",
                "order_number": "O9LQOT1C7C",
                "order_delivery_datetime": "2024-02-07 16:13:30",
                "delivery_type": "pickup",
                "order_status": "accepted",
                "created_date": "2023-12-28 11:39:06",
                "amount": 75.03,
                "delivery_id": 0,
                "order_mode": "online"
            },
            {
                "id": "PP3WmbSH7C0jUKdLohRgOg==",
                "bill_no": "",
                "order_number": "OHLQOSZ7XK",
                "order_delivery_datetime": "2023-12-28 11:37:27",
                "delivery_type": "pickup",
                "order_status": "assigned",
                "created_date": "2023-12-28 11:37:27",
                "amount": 26,
                "delivery_id": 0,
                "order_mode": "online"
            },
            {
                "id": "F09UGz9S343HaQaiqvaeeg==",
                "bill_no": "B00892",
                "order_number": "O8LQGO0LAJ",
                "order_delivery_datetime": "2023-12-22 18:57:32",
                "delivery_type": "delivery",
                "order_status": "completed",
                "created_date": "2023-12-22 18:56:22",
                "amount": 30,
                "delivery_id": 0,
                "order_mode": "online"
            },
            {
                "id": "jSu6tP9pRmG5dE096gJvTg==",
                "bill_no": "",
                "order_number": "OELQ6L4TDQ",
                "order_delivery_datetime": "2023-12-15 17:37:59",
                "delivery_type": "delivery",
                "order_status": "assigned",
                "created_date": "2023-12-15 17:37:59",
                "amount": 29,
                "delivery_id": 0,
                "order_mode": "online"
            },
            {
                "id": "lfGZLf0i4Gwluampo63H9A==",
                "bill_no": "",
                "order_number": "OMLQ6IV126",
                "order_delivery_datetime": "2023-12-15 16:34:22",
                "delivery_type": "delivery",
                "order_status": "assigned",
                "created_date": "2023-12-15 16:34:22",
                "amount": 29,
                "delivery_id": 0,
                "order_mode": "online"
            }
        ],
        "rpp": 20,
        "current_page": 1
    }
}
```
{% endtab %}

{% tab title="200: OK Could not find an order." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 19:06:09",
    "data": {
        "results": [],
        "rpp": 20,
        "current_page": 1
    }
}
```
{% endtab %}
{% endtabs %}

