---
description: To view the summary of the stock.
---

# Stock Summary

## Sales Report&#x20;

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}master/reports/stock_summary`](https://api.evitalrx.in/v1/master/reports/stock_summary)

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                                                                                                                                     |
| ---------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                                                                                                                                                                                                                            |
| manufacturer\_name                       | Array  | A list of manufacturer name(s) to filter the stock summary by                                                                                                                                                                                                                                                   |
| compress\_repsonse                       | String | <p>"<strong>no</strong>": Returns the full, detailed response with all data in a readable format. (default)</p><p>"<strong>yes</strong>": Compresses the response, reducing the size by sending data in a more compact format (array of arrays), which can improve performance when handling large datasets</p> |
| report\_fields                           | Array  | A list of fields to include in the stock summary report. Default includes a set of common fields such as `medicine_id`, `manufacturer_name`, `stock`, `price`, etc.                                                                                                                                             |
| location                                 | Array  | A list of locations where the stock is stored or needs to be filtered by                                                                                                                                                                                                                                        |
| item\_type                               | String | <p><strong>"all"</strong>: Includes all available items. (default)</p><p><strong>"discontinued"</strong>: Only includes items that have been discontinued</p>                                                                                                                                                   |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-12-04 16:33:29",
    "data": {
        "compressed": "no",
        "results": [
            {
                "medicine_code": "MDDRG4997072411",
                "medicine_id": "hKtRHscgbs/zRdGqisi3HA==",
                "manufacturer_name": "TTK Healthcare Ltd",
                "medicine_name": "Dolobest MR 100mg/500mg/250mg Tablet",
                "medicine_category": null,
                "content": "Aceclofenac (100mg) + Paracetamol/Acetaminophen (500mg) + Chlorzoxazone (250mg)",
                "pack_size": "10 Tablets",
                "batch": "ASDASD",
                "margin": 48.42,
                "expiry": "02/27",
                "batch_stock": 0,
                "mrp": 130,
                "total_by_mrp": 0,
                "price_to_retailer": 85.69, // ptr
                "price_to_supplier": 0,
                "total_by_ptr": 0,
                "total_by_pts": 0,
                "landing_price": 81.58,
                "total_by_lp": 0,
                "location": "", // location of the product in pharmacy
                "gst_percentage": 12,
                "hsn_code": "554645",
                "tags": "",
                "size": 10,
                "stock": 154484,
                "medicine_name_alias": "",
                "olddbref": "0",
                "max_quantity": 0,
                "min_quantity": 0
            },
            {
                "medicine_code": "MDDRG4695038199",
                "medicine_id": "oXg3nBR+crfVVlI1JSYsBw==",
                "manufacturer_name": "Staunch Health Care Pvt Ltd",
                "medicine_name": "Laurunam 1000 mg Injection",
                "medicine_category": null,
                "content": "Meropenem (1000mg)",
                "pack_size": "1 Injection",
                "batch": "UHJKL32",
                "margin": 176.36000000000013,
                "expiry": "02/29",
                "batch_stock": 0,
                "mrp": 1857.13,
                "total_by_mrp": 0,
                "price_to_retailer": 1500.69,
                "price_to_supplier": 0,
                "total_by_ptr": 0,
                "total_by_pts": 0,
                "landing_price": 1680.77,
                "total_by_lp": 0,
                "location": "",
                "gst_percentage": 12,
                "hsn_code": "",
                "tags": "",
                "size": 1,
                "stock": 797,
                "medicine_name_alias": "",
                "olddbref": "0",
                "max_quantity": 0,
                "min_quantity": 0
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "item_type must be one of [all, discontinued]",
    "datetime": "2024-12-04 16:34:45",
    "data": null
}
```
{% endtab %}
{% endtabs %}
