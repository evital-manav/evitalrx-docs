---
description: To check if a location is serviceable
---

# Check Serviceability V3

With this API you can check which **location** are **serviceable** and are allowed for placing the order either for **pickup** or **delivery** type order. We check real-time availability of the nearby pharmacy-stores whether they are online or not.

We provide 5 delivery-service primarily:

<table><thead><tr><th width="164.23809814453125">Delivery Service Type</th><th width="174.8092041015625">Delivery Time</th><th>When to Choose Which Delivery Service ?</th></tr></thead><tbody><tr><td>Quick</td><td>within 60 min</td><td><ul><li>Ideal for <strong>Quick-Commerce</strong></li><li>Unique Medicine SKU availability ranges from <strong>Small to Medium</strong> (<em>may vary depending upon the tier of city</em>)</li></ul></td></tr><tr><td>Regular</td><td>within 2 hour</td><td><ul><li>Ideal for <strong>Quick-Commerce</strong></li><li>Unique Medicine SKU availability ranges from <strong>Medium to Large.</strong></li></ul></td></tr><tr><td>In Stock Same Day</td><td>within 8 hours</td><td><ul><li>Ideal for <strong>Insurance-Provider</strong> &#x26; <strong>TPA</strong></li><li>Unique Medicine SKU availability ranges from <strong>Medium to Large.</strong></li></ul></td></tr><tr><td>Same Day</td><td>within 24 hours</td><td><ul><li>Ideal for <strong>Insurance-Provider</strong> &#x26; <strong>TPA</strong></li><li>Unique Medicine SKU availability are <strong>Large.</strong></li></ul></td></tr><tr><td>PAN India</td><td>within 5-7 days<br>vary upon distance</td><td><ul><li>Ideal for General Use</li><li>Unique Medicine SKU availability are <strong>Large.</strong></li></ul></td></tr></tbody></table>

## Things to know

1. Since this API contains real-time availability of the pharmacy-store it is required to refresh the location-token periodically.

* When to refresh the `location_token`
  * Refer to a threshold of 15 min limit.
  * Upon cart-screen loading.
  * Before Placing the order.
  * When patient location is updated or address is changed from address book, cart screen etc.

2. When you can place the order ?

* When you get **serviceable** as `true`

## Get serviceability check

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}fulfillment/orders/check_serviceability_v3`](https://dev-api.evitalrx.in/v1/fulfillment/orders/check_serviceability_v3)

#### Request Body

<table><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>apikey<mark style="color:red;">*</mark></td><td>String</td><td>Authentication Token</td></tr><tr><td>latitude<mark style="color:red;">*</mark></td><td>String</td><td>Latitude of the customer</td></tr><tr><td>longitude<mark style="color:red;">*</mark></td><td>String</td><td>Longitude of the customer</td></tr><tr><td>zipcode<mark style="color:red;">*</mark></td><td>String</td><td>Zipcode of the patient</td></tr><tr><td>service_type<mark style="color:red;">*</mark></td><td>'quick' | 'regular' | 'in_stock_same_day' | 'same_day' | 'pan_india'</td><td><p>Stringified array of service types.</p><p>For eg.</p><pre class="language-postman_json"><code class="lang-postman_json">"[\"quick\",\"regular\", \"in_stock_same_day\",\"same_day\", \"pan_india\"]"
</code></pre></td></tr><tr><td>delivery_type</td><td>'pickup' | 'delivery'</td><td><strong>delivery</strong> (<em>Default</em>): Order will be delivered.<br><strong>pickup</strong> : Order will be of pick-up type.</td></tr><tr><td>full_address</td><td>String</td><td>Full address of  the patient for <br>eg. Office B, 3rd Floor, 4D Square Mall, below PVR Cinema, Motera, Ahmedabad, Gujarat 380005</td></tr></tbody></table>



{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2026-02-14 09:51:58",
    "version": "1.1.547",
    "data": {
        "quick": null,
        "regular": {
            "serviceable": true,
            "error_slug": "",
            "location_token": "lGtSXojVIMwGbrsVqY03B4oboixKAingRNU6lPAIQy/G8L6J9CBmGcTGrx8f/RihijStxJAuMwNf55aMGcSgfrTDU2AKOBcyyhebNW3yc28acHe2sRSSYqtsFqwRfUJDrNQlcht1yEs8+Va6q3jbK69T5piJ7IM/RDpeWWoTvV5o0LFwLueIPfF2EGTMCLXPr191diEc/YmJOJj8hcq/q1XaUyUv0HeUVhe+XC9t6ynlfE2g6q6DlWbTytHQE3OfHyqjWw6QFA41SCo9QmRi/A=="
        },
        "in_stock_same_day": null,
        "same_day": {
            "serviceable": true,
            "error_slug": "",
            "location_token": "lGtSXojVIMwGbrsVqY03B5pG3EIS1dxZwe8yXIiW4NC4B4+02Uu+Iu1EoS5ynBnbz4j7Okw453FONcjxoUYEgzDkbuENC8PbMRNDsk2hNtAwLuTa9kF/VI7Vrs9ddwhtYnOyoDti7K21+BwHIuOP4CJVHu6kvQtFCN7d9XMg1LDzcA+1HcO3B9RXi3ej3nAy+7KhBuUfhI86N48Aewi29xxwEkLVMHfSj6bvvdAAjIdDRvW8NV2mBanAJn8pCfdz4T63PND9YuAL+s761e5Emg=="
        },
        "pan_india": null
    }
}
```
{% endtab %}

{% tab title="200: OK Invalid params" %}
```json
{
    "status_code": "0",
    "status_message": "zipcode is required",
    "datetime": "2025-05-14 10:22:41",
    "version": "1.1.133",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Not Serviceable" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2025-05-14 10:23:22",
    "version": "1.1.133",
    "data": {
        "quick": null,
        "regular": {
            "serviceable": false,
            "error_slug": "no_pharmacy_found",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLVm6SiC2t0JAqdfTAkYsDVaIW1ItSdS37OKMQ5miSYjf"
        },
        "same_day": {
            "serviceable": false,
            "error_slug": "no_pharmacy_found",
            "location_token": "0P6Hm1/BNc7uxzkOSZaBLeGCJnWMLSOhvviSlR4mPlyTurNYbuWd2jb5dWPzlIj5"
        },
        "pan_india": null
    }
}
```
{% endtab %}
{% endtabs %}



## Errors Explanation

* `no_pharmacy_found`&#x20;
  * Currently no pharmacy are available there to take the order or area is not serviceable at the moment.
* `no_pharmacy_found_due_to_off_hours`
  * When pharmacies are there but they are offline or due to their store timing store is closed.

