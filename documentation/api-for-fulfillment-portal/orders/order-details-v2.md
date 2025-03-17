---
description: To view order details
---

# Order Details V2

## Order View

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/view_v2`](https://api.evitalrx.in/v1/fulfillment/orders/view_v2)

#### Request Body

| Name                                        | Type   | Description            |
| ------------------------------------------- | ------ | ---------------------- |
| order\_id<mark style="color:red;">\*</mark> | String | Unique id of the order |
| apikey<mark style="color:red;">\*</mark>    | String | Authentication token   |

{% tabs %}
{% tab title="200: OK Order successfully retrieved." %}
```json
{
    "status_code": "1",
    "status_message": "Order details fetched successfully",
    "datetime": "2025-03-17 16:45:43",
    "version": "1.1.57",
    "data": {
        "order_id": "PSgqibb/4UzPKYBrsv6qqw==",
        "order_number": "OKM80006AU",
        "payment_date": "2025-03-08 14:54:37",
        "payment_status": 3,
        "address_name": "home",
        "address": "Evitalrx Office, 4d Square Mall",
        "address_line2": "",
        "city": "Ahmedabad",
        "zipcode": "380005",
        "created_date": "2025-03-08 14:54:36",
        "redeembalance": 0,
        "prescription_group_id": "",
        "voucher_id": 0,
        "voucher_amount": 0,
        "voucher_discount": 0,
        "prescription_details": [],
        "items": [
            {
                "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                "medicine_name": "Losakind-50 Tablet",
                "size": 10,
                "packing": "Strip",
                "pack_size": "10 Tablet",
                "packing_size": "1 Strip of  10 Tablet",
                "medicine_type": "drug",
                "gst_percentage": 12,
                "quantity": 10,
                "mrp": 42.83,
                "price": 38.55,
                "discount_percentage": 10,
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/62975c5feb174.jpg"
            },
            {
                "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                "medicine_name": "Ltk 50 Tablet",
                "size": 10,
                "packing": "Strip",
                "pack_size": "10 Tablet",
                "packing_size": "1 Strip of  10 Tablet",
                "medicine_type": "drug",
                "gst_percentage": 12,
                "quantity": 2,
                "mrp": 23.5,
                "price": 21.15,
                "discount_percentage": 10,
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/6142edda9e799.jpeg"
            }
        ],
        "charges": {
            "total": {
                "with_discount": 427.8,
                "without_discount": 475.3
            },
            "delivery_charge": {
                "with_discount": 30,
                "without_discount": 30
            },
            "roundoff": {
                "with_discount": 0.2,
                "without_discount": 0.2
            },
            "payable_amount": {
                "with_discount": 458,
                "without_discount": 505.3
            },
            "applied_discounts": {
                "wallet_redeemed": 0,
                "voucher_applied": 0
            }
        },
        "overall_status": "assigned",
        "split_orders": [
            {
                "order_id": 13547,
                "chemist_order_number": "OEM80006E6",
                "chemist_order_id": "/gqBosy53QK574+jpT/auA==",
                "utm_source": "fulfillment",
                "chemist_id": 685,
                "order_status": "cancelled",
                "delivery_id": 0,
                "tracking_url": null,
                "created_date": "2025-03-08 14:54:36",
                "order_delivery_status": null,
                "delivery_estimate_time": 5,
                "verification_images": {
                    "order_packet_verification_images": [],
                    "order_items_verification_images": []
                },
                "invoice_print_url": "http://localhost:8080/evital/invoice/T0VNODAwMDZFNg==/print/",
                "invoice_pdf": "",
                "items": [
                    {
                        "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                        "medicine_name": "Losakind-50 Tablet",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "gst_percentage": 12,
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/62975c5feb174.jpg",
                        "quantity": 10,
                        "mrp": 42.83,
                        "price": 38.55,
                        "discount": 10
                    },
                    {
                        "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                        "medicine_name": "Ltk 50 Tablet",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "gst_percentage": 12,
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/6142edda9e799.jpeg",
                        "quantity": 2,
                        "mrp": 23.5,
                        "price": 21.15,
                        "discount": 10
                    }
                ],
                "chemist_details": {
                    "chemist_id": "EQYmBF/sPyAcIbTXvZ6vRA==",
                    "details": {
                        "pharmacy_name": "Demo Pharmacy",
                        "pharmacy_logo": "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/col6p1dhuv.jpg",
                        "store_photos": [
                            "https://d3cgpvqmlaynvp.cloudfront.net/storage/chemists/kyc/35kddetdv0.png"
                        ],
                        "full_address": "Evital Rx 4d Square Mall, Ahmedabad, Gujarat, India, 380005",
                        "latitude": "23.1025849",
                        "longitude": "72.5953601",
                        "zipcode": "380005",
                        "store_timings": {
                            "fullday_working": "yes",
                            "timings": [
                                {
                                    "id": "tGykhzbp4nsd9zeEAPSYuQ==",
                                    "day_of_week": "monday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "18:00:00"
                                },
                                {
                                    "id": "clyhyxOLPjGvmfppybaa/g==",
                                    "day_of_week": "tuesday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "14:00:00"
                                },
                                {
                                    "id": "rhvyzAAfMfMZzX4Rpt30bA==",
                                    "day_of_week": "wednesday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "20:30:00"
                                },
                                {
                                    "id": "FrJIdUy/EpK93fcLJcNNbg==",
                                    "day_of_week": "thursday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "14:00:00"
                                },
                                {
                                    "id": "xlE5pmGCNWdjVV7pR7foJw==",
                                    "day_of_week": "friday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "14:00:00"
                                },
                                {
                                    "id": "shodTymtXk8SWykPUv80yw==",
                                    "day_of_week": "saturday",
                                    "working": "no",
                                    "start_time": "07:00:00",
                                    "end_time": "19:00:00"
                                },
                                {
                                    "id": "bvtsaFKUrO4nLT1fLD80rQ==",
                                    "day_of_week": "sunday",
                                    "working": "no",
                                    "start_time": "00:00:00",
                                    "end_time": "23:59:59"
                                }
                            ]
                        }
                    }
                }
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Could not find an order matching this query." %}
```json
{
    "status_code": "0",
    "status_message": "No record found",
    "datetime": "2022-12-07 14:30:56",
    "data": null
}
```
{% endtab %}
{% endtabs %}
