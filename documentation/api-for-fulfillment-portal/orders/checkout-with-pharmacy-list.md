# Checkout With Pharmacy List

This API is for pickup type orders only. it provides the cart details of requested items from the pharmacies located near to the patient **latitude-longitude**.

The Cart will be prepared seperately for each pharmacy. It is required for the patient to visit the pharmacy and pickup the order and provide PIN for it.

> The payment to be collected from user may vary from pharmacy-to-pharmacy. So it is recommended that `charges -> payable -> with_discount` is to be used of that pharmacy only.
>
> It is assumed that the availability of items are to be checked from client side for each pharmacy seperately.

### Request Body

<table><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>apikey<mark style="color:red;">*</mark></td><td>String</td><td>Authentication Token</td></tr><tr><td>location_token<mark style="color:red;">*</mark></td><td>String</td><td>Get token from Check Serviceability V3 API</td></tr><tr><td>patient_id</td><td>String</td><td><p>Id to uniquely identify the patient for whom the order is placed.</p><p></p><p>if mobile and patient name is provided, then patient_id is optional.</p></td></tr><tr><td>mobile<mark style="color:red;">*</mark></td><td>String</td><td>Patient's mobile no</td></tr><tr><td>patient_name</td><td>String</td><td>Patient's name</td></tr><tr><td>items<mark style="color:red;">*</mark></td><td>String</td><td><p>Stringified Array of Items.</p><p></p><p>Items should contain at least 1 object. </p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 20 (medicines)</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">"[{\"quantity\":1,\"medicine_id\":\"vVgL6Ggy5tYhqQr1qXOAzA==\"},{\"quantity\":2,\"medicine_id\":\"BXGcaezmfzcQEdh7fZVmUg==\"}]"
</code></pre></td></tr><tr><td>latitude<mark style="color:red;">*</mark></td><td>Number</td><td>Latitude of the customer</td></tr><tr><td>longitude<mark style="color:red;">*</mark></td><td>Number</td><td>Longitude of the customer</td></tr><tr><td>zipcode<mark style="color:red;">*</mark></td><td>String</td><td>Zipcode of the customer</td></tr><tr><td>delivery_type</td><td>String</td><td><p>It can be either delivery or pickup where,</p><p>"delivery" : Order will be delivered to patient address.<br>"pickup" : Order is required to  be picked-up by patient from pharmacy store.</p></td></tr></tbody></table>



{% tabs %}
{% tab title="200: Success" %}


```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2026-02-19 09:41:23",
    "version": "1.1.548",
    "data": [
        {
            "chemist_id": "ff6451049357238b77d5663914fcb99f",
            "pharmacy_name": "API medicals",
            "latitude": "23.1025849",
            "longitude": "72.5953601",
            "full_address": "Cambridge Road, Jogupalya,,Chandkheda,Ahmadabad,Gujarat,380005",
            "distance": 0.03,
            "cart_availability": {
                "charges": {
                    "total": {
                        "with_discount": 58.77,
                        "without_discount": 65.3
                    },
                    "delivery_charge": {
                        "with_discount": 99,
                        "without_discount": 99
                    },
                    "roundoff": {
                        "with_discount": 0.23,
                        "without_discount": 0.23
                    },
                    "payable_amount": {
                        "with_discount": 158,
                        "without_discount": 164.3
                    },
                    "wallet_amount": {
                        "available_amount": 0,
                        "redeemable_amount": 0
                    },
                    "surge_charge": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "handling_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "small_cart_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "delivery_tip_amount": {
                        "with_discount": 0,
                        "without_discount": 0
                    }
                },
                "items": [
                    {
                        "medicine_id": "82fd06a24627f70e3314be757a8b92da",
                        "mrp": 23.5,
                        "price": 21.15,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "10001111",
                        "medicine_category": "drug",
                        "salt_content_id": "d2f70948001fdc95eaacca4eef97fe20",
                        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "medicine_name": "Ltk 50 Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 75.75757575757575,
                        "medicine_type": "drug",
                        "alternatives": [
                            {
                                "medicine_id": "05719c69ece67f371011d87b7d956652",
                                "medicine_slug": "ltk-h-tablet-MDDRG507073852",
                                "content": "Losartan (50mg) + Hydrochlorothiazide (12.5mg)",
                                "is_rx_required": 1,
                                "medicine_name": "LTK-H Tablet",
                                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                                "size": 10,
                                "packing": "Strip",
                                "pack_size": "10 Tablet",
                                "packing_size": "1 Strip of  10 Tablet",
                                "mrp": 136.1,
                                "price": 136.1,
                                "discount_percentage": 0,
                                "medicine_type": "drug",
                                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62566360b108d.jpg",
                                "available_quantity": 1,
                                "available": "yes",
                                "requested_quantity": 1,
                                "popularity_score": 100,
                                "estimated_delivery_tat": "2026-02-19 11:41:22",
                                "service_type": "regular"
                            }
                        ],
                        "is_rx_required": 0,
                        "estimated_delivery_tat": "2026-02-19 11:41:22",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "bd580be86832e6d621a90af5a97380cc",
                        "mrp": 41.8,
                        "price": 37.62,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "30049079",
                        "medicine_category": "drug",
                        "salt_content_id": "cfcf5cabad50deaf9bf4afa33abdf564",
                        "medicine_uses": "Ltk AM Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-am-tablet-MDDRG507073862",
                        "content": "Amlodipine (5mg) + Losartan (50mg)",
                        "medicine_name": "Ltk AM Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459e7daf9d.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 96.96969696969697,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 1,
                        "estimated_delivery_tat": "2026-02-19 11:41:22",
                        "service_type": "regular"
                    }
                ]
            }
        },
        {
            "chemist_id": "bd4ad9791efc8807682d56583ba6a68c",
            "pharmacy_name": "Shree Ganesh Pharmacy",
            "latitude": "23.1027599",
            "longitude": "72.5951718",
            "full_address": "4d Square,Visat,,Chennai,Tamil Nadu,380005",
            "distance": 0,
            "cart_availability": {
                "charges": {
                    "total": {
                        "with_discount": 36.9,
                        "without_discount": 41
                    },
                    "delivery_charge": {
                        "with_discount": 99,
                        "without_discount": 99
                    },
                    "roundoff": {
                        "with_discount": 0.1,
                        "without_discount": 0.1
                    },
                    "payable_amount": {
                        "with_discount": 136,
                        "without_discount": 140
                    },
                    "wallet_amount": {
                        "available_amount": 0,
                        "redeemable_amount": 0
                    },
                    "surge_charge": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "handling_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "small_cart_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "delivery_tip_amount": {
                        "with_discount": 0,
                        "without_discount": 0
                    }
                },
                "items": [
                    {
                        "medicine_id": "82fd06a24627f70e3314be757a8b92da",
                        "mrp": 23.5,
                        "price": 21.15,
                        "discount_percentage": 10,
                        "available": "no",
                        "available_quantity": 0,
                        "requested_quantity": 1,
                        "hsn_code": "10001111",
                        "medicine_category": "drug",
                        "salt_content_id": "d2f70948001fdc95eaacca4eef97fe20",
                        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "medicine_name": "Ltk 50 Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 75.75757575757575,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 0,
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    },
                    {
                        "medicine_id": "bd580be86832e6d621a90af5a97380cc",
                        "mrp": 41,
                        "price": 36.9,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "30049079",
                        "medicine_category": "drug",
                        "salt_content_id": "cfcf5cabad50deaf9bf4afa33abdf564",
                        "medicine_uses": "Ltk AM Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-am-tablet-MDDRG507073862",
                        "content": "Amlodipine (5mg) + Losartan (50mg)",
                        "medicine_name": "Ltk AM Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459e7daf9d.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 96.96969696969697,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 1,
                        "estimated_delivery_tat": "2026-02-19 11:41:22",
                        "service_type": "regular"
                    }
                ]
            }
        },
        {
            "chemist_id": "328c03b679cbc3eb1bcea5ccdb75a901",
            "pharmacy_name": "Motera Main Test",
            "latitude": "23.1027599",
            "longitude": "72.5951718",
            "full_address": "Office B, 3rd Floor, 4d Square Mall,Below Pvr Cinema,Motera,Ahmadabad,Gujarat,380005",
            "distance": 0,
            "cart_availability": {
                "charges": {
                    "total": {
                        "with_discount": 36,
                        "without_discount": 40
                    },
                    "delivery_charge": {
                        "with_discount": 99,
                        "without_discount": 99
                    },
                    "roundoff": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "payable_amount": {
                        "with_discount": 135,
                        "without_discount": 139
                    },
                    "wallet_amount": {
                        "available_amount": 0,
                        "redeemable_amount": 0
                    },
                    "surge_charge": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "handling_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "small_cart_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "delivery_tip_amount": {
                        "with_discount": 0,
                        "without_discount": 0
                    }
                },
                "items": [
                    {
                        "medicine_id": "82fd06a24627f70e3314be757a8b92da",
                        "mrp": 23.5,
                        "price": 21.15,
                        "discount_percentage": 10,
                        "available": "no",
                        "available_quantity": 0,
                        "requested_quantity": 1,
                        "hsn_code": "10001111",
                        "medicine_category": "drug",
                        "salt_content_id": "d2f70948001fdc95eaacca4eef97fe20",
                        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "medicine_name": "Ltk 50 Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 75.75757575757575,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 0,
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    },
                    {
                        "medicine_id": "bd580be86832e6d621a90af5a97380cc",
                        "mrp": 40,
                        "price": 36,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "30049079",
                        "medicine_category": "drug",
                        "salt_content_id": "cfcf5cabad50deaf9bf4afa33abdf564",
                        "medicine_uses": "Ltk AM Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-am-tablet-MDDRG507073862",
                        "content": "Amlodipine (5mg) + Losartan (50mg)",
                        "medicine_name": "Ltk AM Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459e7daf9d.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 96.96969696969697,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 1,
                        "estimated_delivery_tat": "2026-02-19 11:41:23",
                        "service_type": "regular"
                    }
                ]
            }
        },
        {
            "chemist_id": "613dffdcf1009e61289423eb4adaee7b",
            "pharmacy_name": "Maruthi",
            "latitude": "23.10240189701781",
            "longitude": "72.59449108134876",
            "full_address": "3rd Floor, 4d Square Mall, Below Pvr Cinema,Motera,Motera,Ahmedabad,Gujarat,380005",
            "distance": 0.08,
            "cart_availability": {
                "charges": {
                    "total": {
                        "with_discount": 33.17,
                        "without_discount": 36.86
                    },
                    "delivery_charge": {
                        "with_discount": 99,
                        "without_discount": 99
                    },
                    "roundoff": {
                        "with_discount": -0.17,
                        "without_discount": -0.17
                    },
                    "payable_amount": {
                        "with_discount": 132,
                        "without_discount": 135.86
                    },
                    "wallet_amount": {
                        "available_amount": 0,
                        "redeemable_amount": 0
                    },
                    "surge_charge": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "handling_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "small_cart_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "delivery_tip_amount": {
                        "with_discount": 0,
                        "without_discount": 0
                    }
                },
                "items": [
                    {
                        "medicine_id": "82fd06a24627f70e3314be757a8b92da",
                        "mrp": 36.86,
                        "price": 33.17,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "10001111",
                        "medicine_category": "drug",
                        "salt_content_id": "d2f70948001fdc95eaacca4eef97fe20",
                        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "medicine_name": "Ltk 50 Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 75.75757575757575,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 0,
                        "estimated_delivery_tat": "2026-02-19 11:41:23",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "bd580be86832e6d621a90af5a97380cc",
                        "mrp": 41.8,
                        "price": 37.62,
                        "discount_percentage": 10,
                        "available": "no",
                        "available_quantity": 0,
                        "requested_quantity": 1,
                        "hsn_code": "30049079",
                        "medicine_category": "drug",
                        "salt_content_id": "cfcf5cabad50deaf9bf4afa33abdf564",
                        "medicine_uses": "Ltk AM Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-am-tablet-MDDRG507073862",
                        "content": "Amlodipine (5mg) + Losartan (50mg)",
                        "medicine_name": "Ltk AM Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459e7daf9d.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 96.96969696969697,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 1,
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    }
                ]
            }
        },
        {
            "chemist_id": "68b85bf2e20acfcf62d5676370b7846f",
            "pharmacy_name": "Clinikk Ahmedabad",
            "latitude": "23.102161733725655",
            "longitude": "72.59391686466626",
            "full_address": "Shop No 1, Besides Spyker Store, North Plaza,Near 4d Road, Mall,Motera,Ahmadabad,Gujarat,380005",
            "distance": 0.14,
            "cart_availability": {
                "charges": {
                    "total": {
                        "with_discount": 21.15,
                        "without_discount": 23.5
                    },
                    "delivery_charge": {
                        "with_discount": 99,
                        "without_discount": 99
                    },
                    "roundoff": {
                        "with_discount": -0.15,
                        "without_discount": -0.15
                    },
                    "payable_amount": {
                        "with_discount": 120,
                        "without_discount": 122.5
                    },
                    "wallet_amount": {
                        "available_amount": 0,
                        "redeemable_amount": 0
                    },
                    "surge_charge": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "handling_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "small_cart_fee": {
                        "with_discount": 0,
                        "without_discount": 0
                    },
                    "delivery_tip_amount": {
                        "with_discount": 0,
                        "without_discount": 0
                    }
                },
                "items": [
                    {
                        "medicine_id": "82fd06a24627f70e3314be757a8b92da",
                        "mrp": 23.5,
                        "price": 21.15,
                        "discount_percentage": 10,
                        "available": "yes",
                        "available_quantity": 1,
                        "requested_quantity": 1,
                        "hsn_code": "10001111",
                        "medicine_category": "drug",
                        "salt_content_id": "d2f70948001fdc95eaacca4eef97fe20",
                        "medicine_uses": "Ltk 50 Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "medicine_name": "Ltk 50 Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 75.75757575757575,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 0,
                        "estimated_delivery_tat": "2026-02-19 11:41:23",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "bd580be86832e6d621a90af5a97380cc",
                        "mrp": 41.8,
                        "price": 37.62,
                        "discount_percentage": 10,
                        "available": "no",
                        "available_quantity": 0,
                        "requested_quantity": 1,
                        "hsn_code": "30049079",
                        "medicine_category": "drug",
                        "salt_content_id": "cfcf5cabad50deaf9bf4afa33abdf564",
                        "medicine_uses": "Ltk AM Tablet is used in the treatment of <a href='/diseases/high-blood-pressure-68'>high blood pressure</a>.",
                        "medicine_slug": "ltk-am-tablet-MDDRG507073862",
                        "content": "Amlodipine (5mg) + Losartan (50mg)",
                        "medicine_name": "Ltk AM Tablet",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459e7daf9d.jpg",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "popularity_score": 96.96969696969697,
                        "medicine_type": "drug",
                        "alternatives": [],
                        "is_rx_required": 1,
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    }
                ]
            }
        }
    ]
}
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}
