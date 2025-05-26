---
description: To check availability of the items.
---

# Checkout V3

## Get the availability of medicines

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/checkout_v3`](https://api.evitalrx.in/v1/fulfillment/orders/checkout_v3)

For the medicines which are out of stock, available alternative medicines will be provided.

#### Request Body

| Name                                              | Type    | Description                                                                                                                                                                                                                                                                                                                                                              |
| ------------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark>          | String  | Authentication Token                                                                                                                                                                                                                                                                                                                                                     |
| location\_token<mark style="color:red;">\*</mark> | String  | Get token fro Check Serviceability V3 API                                                                                                                                                                                                                                                                                                                                |
| patient\_id                                       | String  | Id to uniquely identify the patient for whom the order is placed                                                                                                                                                                                                                                                                                                         |
| mobile                                            | String  | Patient's mobile no                                                                                                                                                                                                                                                                                                                                                      |
| patient\_name                                     | String  | Patient's name                                                                                                                                                                                                                                                                                                                                                           |
| items<mark style="color:red;">\*</mark>           | String  | <p>Stringified Array of Items.</p><p></p><p>Items should contain at least 1 object. </p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 20 (medicines)</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">"[{\"quantity\":1,\"medicine_id\":\"vVgL6Ggy5tYhqQr1qXOAzA==\"},{\"quantity\":2,\"medicine_id\":\"BXGcaezmfzcQEdh7fZVmUg==\"}]"
</code></pre> |
| latitude<mark style="color:red;">\*</mark>        | Number  | Latitude of the customer                                                                                                                                                                                                                                                                                                                                                 |
| longitude<mark style="color:red;">\*</mark>       | Number  | Longitude of the customer                                                                                                                                                                                                                                                                                                                                                |
| zipcode<mark style="color:red;">\*</mark>         | String  | Zipcode of the customer                                                                                                                                                                                                                                                                                                                                                  |
| distance                                          | Number  | <p>Distance of fulfillment.<br><br>radius of search area for search provided item</p>                                                                                                                                                                                                                                                                                    |
| find\_alternative                                 | Boolean | Flag to get item alternatives                                                                                                                                                                                                                                                                                                                                            |



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-03-11 12:48:19",
    "version": "1.1.49",
    "data": {
        "shipping_charges": 30,
        "chemist_details_list": [
            {
                "chemist_id": "EQYmBF/sPyAcIbTXvZ6vRA==",
                "distance": 0,
                "chemist_details": {
                    "pharmacy_name": "Bhargav Pharmacy",
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
        ],
        "items": [
            {
                "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                "mrp": 42.83,
                "price": 38.55,
                "discount_percentage": 10,
                "available": "yes",
                "estimated_delivery_tat": "2025-05-14 10:45:50",
                "service_type": "regular",
                "alternatives": [
                    {
                        "approved": 0,
                        "available_for_patient": "yes",
                        "cess_percentage": 0,
                        "requested_by_entity": "chemist",
                        "content": "Paracetamol (650mg)",
                        "dosage_type": "tablet",
                        "gst_percentage": 12,
                        "gtin_number": "",
                        "hsn_code": "30049099",
                        "image": "https://d2ffmswuyj0h1d.cloudfront.net/storage/medicines/thumb/60ae1dc73132f.jpg",
                        "manufacturer_name": "Hetero Drugs Ltd",
                        "medicine_id": "PDqfWw+enNR0w5U23KOsZg==",
                        "medicine_name": "Lanol ER Tablet (10 Tablet)",
                        "medicine_name_suggest": "Lanol ER Tablet (10 Tablet)",
                        "medicine_type": "drug",
                        "mrp": 22.4,
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "price": 20.16,
                        "discount_percentage": 10,
                        "salt_content_id": 197,
                        "schedule_type": "H",
                        "size": 10,
                        "slug": "lanol-er-tablet-10-tablet-MDDRG2183024649",
                        "is_rx_required": 1,
                        "primary_category_id": 819,
                        "popularity_score": 99.83337266934151
                    }
                ]
            },
            {
                "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                "mrp": 23.5,
                "price": 21.15,
                "discount_percentage": 10,
                "available": "yes",
                "estimated_delivery_tat": "2025-05-14 10:45:50",
                "service_type": "same_day"
                "alternatives": []
            },
            {
                "medicine_id": "b1ad0N315wy4+UDhhT5FjA==",
                "mrp": 23.5,
                "price": 21.15,
                "discount_percentage": 10,
                "available": "no",
                "alternatives": []
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Invalid params" %}
```json
{
    "status_code": "0",
    "status_message": "longitude is required",
    "datetime": "2023-02-15 12:46:54",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK No pharmacy found" %}
```json
{
    "status_code": "0",
    "status_message": "No Pharmacies found near by your location",
    "datetime": "2023-02-15 12:37:11",
    "data": null
}
```
{% endtab %}
{% endtabs %}
