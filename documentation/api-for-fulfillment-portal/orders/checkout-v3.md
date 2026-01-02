---
description: To check availability of the items.
---

# Checkout V3

This API provides availability of medicines with alternatives. And calculates the total cart value.

## Get the availability of medicines

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/checkout_v3`](https://dev-api.evitalrx.in/v1/fulfillment/orders/checkout_v3)

For the medicines which are out of stock, available alternative medicines will be provided.

> In API request, You need to pass either provide **patient\_id** or **mobile & patient\_name**.

#### Charges Breakdown Explanation

* `with_discount` represents the **actual payable amount** after offers.
* `without_discount` is used for **price comparison and savings calculation**.
* On Collecting Payment from patient always use `payable_amount.with_discount`&#x20;



**charges-total-with\_discount** = This amount is summation of items `price * quantity`.

**charges-total-without\_discount** = This amount is summation of items `mrp * quantity` .

**payable\_amount.without\_discount** calculation

```markdown
payable_amount.without_discount =
    total.without_discount
  + delivery_charge.without_discount
  + surge_charge.without_discount
  + handling_fee.without_discount
  + small_cart_fee.without_discount
  + delivery_tip_amount.without_discount
```

**payable\_amount.with\_discount** calculation

```markdown
 payable_amount.with_discount =
       total.with_discount
      + delivery_charge.with_discount
      + surge_charge.with_discount
      + handling_fee.with_discount
      + small_cart_fee.with_discount
      + delivery_tip_amount.with_discount
```



#### Request Body

<table><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>apikey<mark style="color:red;">*</mark></td><td>String</td><td>Authentication Token</td></tr><tr><td>location_token<mark style="color:red;">*</mark></td><td>String</td><td>Get token from Check Serviceability V3 API</td></tr><tr><td>patient_id<mark style="color:red;">*</mark></td><td>String</td><td><p>Id to uniquely identify the patient for whom the order is placed.</p><p></p><p>if mobile and patient name is provided, then patient_id is optional.</p></td></tr><tr><td>mobile</td><td>String</td><td>Patient's mobile no</td></tr><tr><td>patient_name</td><td>String</td><td>Patient's name</td></tr><tr><td>items<mark style="color:red;">*</mark></td><td>String</td><td><p>Stringified Array of Items.</p><p></p><p>Items should contain at least 1 object. </p><p></p><p>MIN: 1 (medicines)</p><p>MAX: 20 (medicines)</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">"[{\"quantity\":1,\"medicine_id\":\"vVgL6Ggy5tYhqQr1qXOAzA==\"},{\"quantity\":2,\"medicine_id\":\"BXGcaezmfzcQEdh7fZVmUg==\"}]"
</code></pre></td></tr><tr><td>latitude<mark style="color:red;">*</mark></td><td>Number</td><td>Latitude of the customer</td></tr><tr><td>longitude<mark style="color:red;">*</mark></td><td>Number</td><td>Longitude of the customer</td></tr><tr><td>zipcode<mark style="color:red;">*</mark></td><td>String</td><td>Zipcode of the customer</td></tr><tr><td>find_alternative</td><td>Boolean</td><td>Flag to get item alternatives</td></tr><tr><td>show_cart_options</td><td>Boolean</td><td>To know alternate cart items options.</td></tr><tr><td>delivery_type</td><td>String</td><td><p>It can be either delivery ot pickup where,</p><p>"delivery" : Order will be delivered.<br>"pickup" : Order will be of pick-up type.</p></td></tr></tbody></table>



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-07-28 16:13:52",
    "version": "1.1.254",
    "data": {
        "shipping_charges": 50,
        "charges": {
            "total": {
                "with_discount": 355.8,
                "without_discount": 355.8
            },
            "delivery_charge": {
                "with_discount": 69,
                "without_discount": 69
            },
            "roundoff": {
                "with_discount": 0.2,
                "without_discount": 0.2
            },
            "payable_amount": {
                "with_discount": 425,
                "without_discount": 424.8
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
                "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                "mrp": 42.83,
                "price": 42.83,
                "discount_percentage": 0,
                "available": "yes",
                "available_quantity": 2,
                "requested_quantity": 2,
                "alternatives": [
                    {
                        "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 0,
                        "medicine_name": "Ltk 50 Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "mrp": 25,
                        "price": 25,
                        "discount_percentage": 0,
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/6142edda9e799.jpeg",
                        "available_quantity": 2,
                        "available": "yes",
                        "requested_quantity": 2,
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "biijdBcG6mMCg+g8mrHGFA==",
                        "medicine_slug": "losfirst-50mg-tablet-MDDRG5503084143",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 1,
                        "medicine_name": "Losfirst 50 mg Tablet",
                        "manufacturer_name": "Zyphar's Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablets",
                        "packing_size": "10 tablets in 1 strip",
                        "mrp": 44.63,
                        "price": 41.06,
                        "discount_percentage": 8,
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                        "available_quantity": 2,
                        "available": "yes",
                        "requested_quantity": 2,
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    }
                ],
                "estimated_delivery_tat": "2025-07-28 18:13:52",
                "service_type": "regular"
            },
            {
                "medicine_id": "eYlGilhNCz4CDs/NqrnbcQ==",
                "mrp": 12.8,
                "price": 11.52,
                "discount_percentage": 10,
                "available": "yes",
                "available_quantity": 5,
                "requested_quantity": 5,
                "alternatives": [],
                "estimated_delivery_tat": "2025-07-28 18:13:52",
                "service_type": "regular"
            },
            {
                "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                "mrp": 25,
                "price": 23,
                "discount_percentage": 8,
                "available": "yes",
                "available_quantity": 2,
                "requested_quantity": 2,
                "alternatives": [],
                "estimated_delivery_tat": "2025-07-28 18:13:52",
                "service_type": "regular"
            },
            {
                "medicine_id": "adUASNSP6SnY/XbyHLkruw==",
                "mrp": 65.21,
                "price": 58.69,
                "discount_percentage": 10,
                "available": "no",
                "available_quantity": 0,
                "requested_quantity": 2,
                "alternatives": [],
                "estimated_delivery_tat": "",
                "service_type": ""
            }
        ],
        "cart_options": [
            {
                "label": "quick_same_medicines",
                "title": "Quick Delivery with Same Medicines",
                "available_item_count": 3,
                "total_mrp": 199.66,
                "total_discount": 10.4,
                "total_price": 189.26,
                "shipping": 50,
                "payable_amount": 239.26,
                "items": [
                    {
                        "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                        "mrp": 42.83,
                        "price": 42.83,
                        "discount_percentage": 0,
                        "requested_quantity": 2,
                        "amount": 85.66,
                        "medicine_slug": "losakind-50-tablet-MDDRG286667590",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 1,
                        "medicine_name": "Losakind-50 Tablet",
                        "manufacturer_name": "Mankind Pharma Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62975c5feb174.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 2,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "eYlGilhNCz4CDs/NqrnbcQ==",
                        "mrp": 12.8,
                        "price": 11.52,
                        "discount_percentage": 10,
                        "requested_quantity": 5,
                        "amount": 57.6,
                        "medicine_slug": "ltk-25mg-tablet-MDDRG507073860",
                        "content": "Losartan (25mg)",
                        "is_rx_required": 1,
                        "medicine_name": "Ltk 25mg Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 5,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                        "mrp": 25,
                        "price": 23,
                        "discount_percentage": 8,
                        "requested_quantity": 2,
                        "amount": 46,
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 0,
                        "medicine_name": "Ltk 50 Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/6142edda9e799.jpeg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 2,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "adUASNSP6SnY/XbyHLkruw==",
                        "mrp": 65.21,
                        "price": 58.69,
                        "discount_percentage": 10,
                        "requested_quantity": 2,
                        "amount": 0,
                        "medicine_slug": "dytor-----5",
                        "content": "",
                        "is_rx_required": 0,
                        "medicine_name": "Dytor -   5",
                        "manufacturer_name": "1mg Technologies Pvt. Ltd",
                        "size": 15,
                        "packing": "15",
                        "pack_size": "15T",
                        "packing_size": "15T",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 0,
                        "available": "no",
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    }
                ]
            },
            {
                "label": "quick_alternative_medicines",
                "title": "Quick Delivery with Alternative Medicines",
                "available_item_count": 3,
                "total_mrp": 199.66,
                "total_discount": 10.4,
                "total_price": 189.26,
                "shipping": 50,
                "payable_amount": 239.26,
                "items": [
                    {
                        "medicine_id": "EvM8wa0vXyjsi2JZnNKXrA==",
                        "mrp": 42.83,
                        "price": 42.83,
                        "discount_percentage": 0,
                        "requested_quantity": 2,
                        "amount": 85.66,
                        "medicine_slug": "losakind-50-tablet-MDDRG286667590",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 1,
                        "medicine_name": "Losakind-50 Tablet",
                        "manufacturer_name": "Mankind Pharma Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62975c5feb174.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 2,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "eYlGilhNCz4CDs/NqrnbcQ==",
                        "mrp": 12.8,
                        "price": 11.52,
                        "discount_percentage": 10,
                        "requested_quantity": 5,
                        "amount": 57.6,
                        "medicine_slug": "ltk-25mg-tablet-MDDRG507073860",
                        "content": "Losartan (25mg)",
                        "is_rx_required": 1,
                        "medicine_name": "Ltk 25mg Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/60c459646117f.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 5,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "y1sw0N315wy4+UDhhT5FjA==",
                        "mrp": 25,
                        "price": 23,
                        "discount_percentage": 8,
                        "requested_quantity": 2,
                        "amount": 46,
                        "medicine_slug": "ltk-50-tablet-MDDRG507073861",
                        "content": "Losartan (50mg)",
                        "is_rx_required": 0,
                        "medicine_name": "Ltk 50 Tablet",
                        "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                        "size": 10,
                        "packing": "Strip",
                        "pack_size": "10 Tablet",
                        "packing_size": "1 Strip of  10 Tablet",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/6142edda9e799.jpeg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 2,
                        "available": "yes",
                        "estimated_delivery_tat": "2025-07-28 18:13:52",
                        "service_type": "regular"
                    },
                    {
                        "medicine_id": "adUASNSP6SnY/XbyHLkruw==",
                        "mrp": 65.21,
                        "price": 58.69,
                        "discount_percentage": 10,
                        "requested_quantity": 2,
                        "amount": 0,
                        "medicine_slug": "dytor-----5",
                        "content": "",
                        "is_rx_required": 0,
                        "medicine_name": "Dytor -   5",
                        "manufacturer_name": "1mg Technologies Pvt. Ltd",
                        "size": 15,
                        "packing": "15",
                        "pack_size": "15T",
                        "packing_size": "15T",
                        "medicine_type": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                        "is_swap_available": "no",
                        "swap_medicines": [],
                        "available_quantity": 0,
                        "available": "no",
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    }
                ]
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
