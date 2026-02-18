# Checkout By Content

This API provides the finds the medicines which matches the combination of **salt-content & dosage-type.**

The `salt-content-id` & `dosage-type` can be found from [medicine search](../medicines/search-products.md) API.

### Request Body

<table><thead><tr><th>Key</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>apikey<mark style="color:$danger;">*</mark></td><td>String</td><td>Authentication Token</td></tr><tr><td>location_token<mark style="color:$danger;">*</mark></td><td>String</td><td>It can be obtain from Check Serviceability API</td></tr><tr><td>latitude<mark style="color:$danger;">*</mark></td><td>Number</td><td>Latitude of the Customer</td></tr><tr><td>longitude<mark style="color:$danger;">*</mark></td><td>Number</td><td>Longitude of the Customer</td></tr><tr><td>zipcode<mark style="color:$danger;">*</mark></td><td>String</td><td>Zipcode of the Customer</td></tr><tr><td>mobile<mark style="color:$danger;">*</mark></td><td>String</td><td>Customer's mobile number</td></tr><tr><td>patient_name</td><td>Number</td><td>Customer's Name</td></tr><tr><td>show_cart_options</td><td>Boolean</td><td>To know alternate cart items options.</td></tr><tr><td>find_alternative</td><td>Boolean</td><td>Flag to get item alternatives</td></tr><tr><td>contents<mark style="color:$danger;">*</mark></td><td>Array[salt_content_id, dosage_type, quantity]</td><td><p>Stringified array of contents<br>example:</p><pre class="language-json"><code class="lang-json">"[{\"salt_content_id\":\"+qIGHQHPc9AJh9QUPHyMSA==\",\"dosage_type\":\"tablet\",\"quantity\":1}]"
</code></pre></td></tr></tbody></table>



{% tabs %}
{% tab title="200: Success" %}


```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2026-02-18 09:52:24",
    "version": "1.1.548",
    "data": {
        "shipping_charges": 99,
        "charges": {
            "total": {
                "with_discount": 30.74,
                "without_discount": 30.74
            },
            "delivery_charge": {
                "with_discount": 99,
                "without_discount": 99
            },
            "roundoff": {
                "with_discount": 0.26,
                "without_discount": 0.26
            },
            "payable_amount": {
                "with_discount": 130,
                "without_discount": 130
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
                "medicine_id": "X1P9/F3XVunOtftRNNCyHA==",
                "medicine_slug": "dolo-650-tablet-M00234T",
                "content": "Paracetamol (650mg)",
                "salt_content_id": "+qIGHQHPc9AJh9QUPHyMSA==",
                "is_rx_required": 0,
                "medicine_name": "Dolo 650 Tablet",
                "manufacturer_name": "Micro Labs Ltd",
                "popularity_score": 72.72727272727273,
                "size": 15,
                "packing": "Strip",
                "pack_size": "15 Tablet",
                "packing_size": "1 Strip of  15 Tablet",
                "mrp": 30.74,
                "price": 30.74,
                "discount_percentage": 0,
                "medicine_type": "drug",
                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62d4e09cd4dd3.jpg",
                "available_quantity": 1,
                "available": "yes",
                "requested_quantity": 1,
                "partner_margin_percentage": 0,
                "estimated_delivery_tat": "2026-02-18 11:52:24",
                "service_type": "regular",
                "alternatives": [
                    {
                        "medicine_id": "MphSE/QcD2dlcu9zdeV8xw==",
                        "mrp": 33,
                        "price": 33,
                        "discount_percentage": 0,
                        "available": "no",
                        "available_quantity": 0,
                        "requested_quantity": 1,
                        "hsn_code": "0",
                        "medicine_category": "drug",
                        "salt_content_id": "+qIGHQHPc9AJh9QUPHyMSA==",
                        "medicine_uses": "",
                        "medicine_slug": "calpol-650-tablet-15-tablet-MDDRG19631963758",
                        "popularity_score": 0,
                        "content": "Paracetamol (650mg)",
                        "medicine_name": "Calpol 650 Tablet (15 Tablet)",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                        "size": 15,
                        "packing": "Strip",
                        "pack_size": "15 Tablet",
                        "packing_size": "1 Strip of  15 Tablet",
                        "medicine_type": "drug",
                        "is_rx_required": 0,
                        "partner_margin_percentage": 20,
                        "estimated_delivery_tat": "",
                        "service_type": ""
                    }
                ]
            }
        ],
        "cart_options": [
            {
                "label": "quick_same_medicines",
                "title": "Quick Delivery with Same Medicines",
                "available_item_count": 0,
                "total_mrp": 0,
                "total_discount": 0,
                "total_price": 0,
                "shipping": 0,
                "payable_amount": 0,
                "items": [
                    {
                        "medicine_id": "MphSE/QcD2dlcu9zdeV8xw==",
                        "mrp": 33,
                        "price": 33,
                        "discount_percentage": 0,
                        "requested_quantity": 1,
                        "amount": 0,
                        "medicine_slug": "calpol-650-tablet-15-tablet-MDDRG19631963758",
                        "content": "Paracetamol (650mg)",
                        "is_rx_required": 0,
                        "medicine_name": "Calpol 650 Tablet (15 Tablet)",
                        "manufacturer_name": "Glaxo SmithKline Pharmaceuticals Ltd",
                        "popularity_score": 0,
                        "available_for_patient": "no",
                        "size": 15,
                        "packing": "Strip",
                        "pack_size": "15 Tablet",
                        "packing_size": "1 Strip of  15 Tablet",
                        "medicine_type": "drug",
                        "medicine_category": "drug",
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
                "available_item_count": 1,
                "total_mrp": 30.74,
                "total_discount": 0,
                "total_price": 30.74,
                "shipping": 99,
                "payable_amount": 129.74,
                "items": [
                    {
                        "medicine_id": "MphSE/QcD2dlcu9zdeV8xw==",
                        "mrp": 33,
                        "price": 33,
                        "discount_percentage": 0,
                        "requested_quantity": 1,
                        "amount": 0,
                        "medicine_slug": "calpol-650-tablet-15-tablet-MDDRG19631963758",
                        "content": "Paracetamol (650mg)",
                        "is_rx_required": 0,
                        "medicine_name": "Calpol 650 Tablet (15 Tablet)",
                        "manufacturer_name": "Glaxo SmithKline Pharmaceuticals Ltd",
                        "popularity_score": 0,
                        "available_for_patient": "no",
                        "size": 15,
                        "packing": "Strip",
                        "pack_size": "15 Tablet",
                        "packing_size": "1 Strip of  15 Tablet",
                        "medicine_type": "drug",
                        "medicine_category": "drug",
                        "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/default.jpg",
                        "is_swap_available": "yes",
                        "swap_medicines": [
                            {
                                "medicine_id": "X1P9/F3XVunOtftRNNCyHA==",
                                "medicine_slug": "dolo-650-tablet-M00234T",
                                "content": "Paracetamol (650mg)",
                                "is_rx_required": 0,
                                "medicine_name": "Dolo 650 Tablet",
                                "manufacturer_name": "Micro Labs Ltd",
                                "popularity_score": 72.72727272727273,
                                "size": 15,
                                "packing": "Strip",
                                "pack_size": "15 Tablet",
                                "packing_size": "1 Strip of  15 Tablet",
                                "mrp": 30.74,
                                "price": 30.74,
                                "discount_percentage": 0,
                                "medicine_type": "drug",
                                "medicine_category": "drug",
                                "available_for_patient": "yes",
                                "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/itemoriginalcopy/medicines/62d4e09cd4dd3.jpg",
                                "requested_quantity": 1,
                                "amount": 30.74,
                                "available_quantity": 1,
                                "available": "yes",
                                "estimated_delivery_tat": "2026-02-18 11:52:24",
                                "service_type": "regular"
                            }
                        ],
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

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}
