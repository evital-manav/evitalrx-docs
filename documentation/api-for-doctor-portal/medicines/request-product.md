---
description: To request a product, which is not available at eVitalRx.
---

# Request Product

## Request Product

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/request_medicine`

#### Request Body

<table><thead><tr><th width="285">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>apikey<mark style="color:red;">*</mark></td><td>String</td><td>Authentication Token</td></tr><tr><td>medicine_name<mark style="color:red;">*</mark></td><td>String</td><td>Product Name</td></tr><tr><td>gtin_number</td><td>String</td><td>Product's GTIN Number</td></tr><tr><td>hsn_code</td><td>String</td><td><p>Product's HSN Number</p><p>Min Length: 3</p><p>Max Length: 8</p></td></tr><tr><td>manufacturer_name<mark style="color:red;">*</mark></td><td>String</td><td>Product's Manufacturer Name</td></tr><tr><td>packaging<mark style="color:red;">*</mark></td><td>String</td><td><p>Product's Packaging</p><p></p><p>Packaging: strip, bottle, packet, piece, tube, etc.</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>Then pass <strong>"packaging":  "tube"</strong></p></td></tr><tr><td>mrp<mark style="color:red;">*</mark></td><td>Number</td><td>Price of the Product</td></tr><tr><td>unit</td><td>String</td><td><p>Unit for the measurement of the Product</p><p></p><p>Units: gm, ml, tablets, capsules, etc.</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>Then pass <strong>"unit":  "gm"</strong></p></td></tr><tr><td>weightage</td><td>Number</td><td><p>Weightage of the Product:</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>pass <strong>"weightage":  100</strong></p></td></tr><tr><td>gst_percentage</td><td>Number</td><td><p>GST Percentage of the Product:</p><p>Valid values: 0, 5, 12, 18, 28</p></td></tr><tr><td>os</td><td>String</td><td>web</td></tr><tr><td>image<mark style="color:red;">*</mark></td><td>File</td><td>Back photo of the Product.</td></tr><tr><td>image<mark style="color:red;">*</mark></td><td>File</td><td>Front photo of the Product.</td></tr></tbody></table>

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-06 17:30:56",
    "data": {
        "medicine_id": "sWCoyp2jvgEx9ul1CBOuFA==",
        "medicine_type": "",
        "packing_size": "1 Tube of 100 Gm",
        "pack_size": "100 Gm",
        "manufacturer_name": "",
        "hsn_code": "",
        "gst_percentage": 0,
        "gtin_number": "",
        "mrp": 100,
        "medicine_name": "Himalaya Fairness Cream"
    }
}
```
{% endtab %}

{% tab title="200: OK Images not found" %}
```json
{
    "status_code": "0",
    "status_message": "Medicine images not found",
    "datetime": "2022-12-06 17:31:17",
    "data": null
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"manufacturer_name\" is not allowed to be empty",
    "datetime": "2022-12-06 17:32:05",
    "data": null
}
```
{% endtab %}
{% endtabs %}
