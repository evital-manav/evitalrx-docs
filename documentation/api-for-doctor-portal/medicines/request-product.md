---
description: To request a product, which is not available at eVitalRx.
---

# Request Product

## Request Product

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/medicines/request_medicine`

#### Request Body

| Name                                                 | Type   | Description                                                                                                                                                                                       |
| ---------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>             | String | Authentication Token                                                                                                                                                                              |
| medicine\_name<mark style="color:red;">\*</mark>     | String | Product Name                                                                                                                                                                                      |
| gtin\_number                                         | String | Product's GTIN Number                                                                                                                                                                             |
| hsn\_code                                            | String | <p>Product's HSN Number</p><p>Min Length: 3</p><p>Max Length: 8</p>                                                                                                                               |
| manufacturer\_name<mark style="color:red;">\*</mark> | String | Product's Manufacturer Name                                                                                                                                                                       |
| packaging<mark style="color:red;">\*</mark>          | String | <p>Product's Packaging</p><p></p><p>Packaging: strip, bottle, packet, piece, tube, etc.</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>Then pass <strong>"packaging":  "tube"</strong></p> |
| mrp<mark style="color:red;">\*</mark>                | Number | Price of the Product                                                                                                                                                                              |
| unit                                                 | String | <p>Unit for the measurement of the Product</p><p></p><p>Units: gm, ml, tablets, capsules, etc.</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>Then pass <strong>"unit":  "gm"</strong></p> |
| weightage                                            | Number | <p>Weightage of the Product:</p><p></p><p>Examples: Himalaya Cream is 100gm.</p><p>pass <strong>"weightage":  100</strong></p>                                                                    |
| gst\_percentage                                      | Number | <p>GST Percentage of the Product:</p><p>Valid values: 0, 5, 12, 18, 28</p>                                                                                                                        |
| os                                                   | String | web                                                                                                                                                                                               |
| image<mark style="color:red;">\*</mark>              | File   | Back photo of the Product.                                                                                                                                                                        |
| image<mark style="color:red;">\*</mark>              | File   | Front photo of the Product.                                                                                                                                                                       |

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
