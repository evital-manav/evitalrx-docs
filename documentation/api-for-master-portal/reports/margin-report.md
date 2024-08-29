---
description: To view Margin of Sales/Sales Return
---

# Margin Report

## Margin Report&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/master/reports/margin_report`

#### Request Body

| Name                                          | Type   | Description                                                                                                                                                                                                                                    |
| --------------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| start\_date<mark style="color:red;">\*</mark> | String | <p>Start Date of the report. Must be less than equals to current Date or End Date.</p><p></p><p>Format = YYYY-MM-DD</p>                                                                                                                        |
| end\_date<mark style="color:red;">\*</mark>   | String | <p>End Date of the report. Must be greater than equals to Start Date and less than equals to current Date.</p><p></p><p>Format = YYYY-MM-DD</p><p></p><p>The duration between End Date and Start Date must be less than equals to 31 days.</p> |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                                                                                                                           |
| view\_by                                      | String | <p>item_wise | bill_item_wise</p><p></p><p>bill_item_wise: Show the margin on Sales bills.</p><p>item_wise: Show the margin on items.</p><p></p><p>Default Value: bill_item_wise</p><p></p>                                                    |
| requested\_by                                 | String | <p>sales | sale_return</p><p></p><p>sales: Show Sales Margin Report. </p><p>sale_return: Show Sales Return Margin Report.</p><p></p><p>Default: sales</p>                                                                                      |
| tags                                          | String | <p>["headache", "painkiller"]</p><p></p><p>filter by tags in the bill_item_wise report.</p>                                                                                                                                                    |
| child\_chemist\_code                          | String | <p>chemist_code of Child Chemist. </p><p></p><p>It will show the margin report of the child chemist.</p>                                                                                                                                       |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-01-09 15:06:22",
    "data": {
        "type": "sales",
        "current_page": 1,
        "summary": {
            "total_purchase": 138.88,
            "total_sell": 225.6,
            "total_net_gst": 4.56,
            "profit": 82.16,
            "margin": 38.5
        },
        "results": [
            {
                "order_id": "hXdqB4ImyDFgNkqnvDQfSg==",
                "created_date": "2022-11-08 18:48:23",
                "patient_name": "Poojan Mehta",
                "bill_no": "23",
                "patient_id": "jbe37VCyuofdSgqVfzUAEA==",
                "medicine_id": "gv0GokYn9w4zFL51eouS2g==",
                "total_quantity_sold": 10,
                "gstpercentage": 5,
                "mrp": 112,
                "discount": 10,
                "current_stock": 90,
                "total_selling_price": 100.8,
                "total_landing_price": 10.08,
                "total_sales_gst": 4.8,
                "order_by_id": "+93Y8e1zYBSOwcnRNboSJw==",
                "order_by_entity": "chemist",
                "tag": [
                    "headache"
                ],
                "medicine_name": "Ltk 50 Tablet",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "size": 10,
                "pack_size": "10 Tablets",
                "total_purchase_gst": 0.48,
                "total_net_gst": 4.32,
                "taxable_purchase_amount": 9.6,
                "taxable_sales_amount": 96,
                "profit": 86.4,
                "margin": 90
            },
            {
                "order_id": "yl4XZ5EZ9HHUEil31DBWzw==",
                "created_date": "2022-12-01 18:09:48",
                "patient_name": "Ronak Dunzo",
                "bill_no": "24",
                "patient_id": "zRC97Kh3xOMVdHZKkyZRVA==",
                "medicine_id": "BXGcaezmfzcQEdh7fZVmUg==",
                "total_quantity_sold": 15,
                "gstpercentage": 12,
                "mrp": 24,
                "discount": 0,
                "current_stock": 607,
                "total_selling_price": 24,
                "total_landing_price": 16.8,
                "total_sales_gst": 2.57,
                "order_by_id": "+93Y8e1zYBSOwcnRNboSJw==",
                "order_by_entity": "chemist",
                "tag": [
                    "headache"
                ],
                "medicine_name": "LTK-H Tablet 5",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "size": 15,
                "pack_size": "15 Tablet",
                "total_purchase_gst": 1.8,
                "total_net_gst": 0.77,
                "taxable_purchase_amount": 15,
                "taxable_sales_amount": 21.43,
                "profit": 6.43,
                "margin": 30
            },
            {
                "order_id": "3+uJ2X8XmtbtDwKB1Pa+BQ==",
                "created_date": "2022-11-08 17:13:59",
                "patient_name": "Poojan Mehta",
                "bill_no": "22",
                "patient_id": "jbe37VCyuofdSgqVfzUAEA==",
                "medicine_id": "gv0GokYn9w4zFL51eouS2g==",
                "total_quantity_sold": 10,
                "gstpercentage": 5,
                "mrp": 112,
                "discount": 10,
                "current_stock": 90,
                "total_selling_price": 100.8,
                "total_landing_price": 112,
                "total_sales_gst": 4.8,
                "order_by_id": "+93Y8e1zYBSOwcnRNboSJw==",
                "order_by_entity": "chemist",
                "tag": [
                    "headache"
                ],
                "medicine_name": "Ltk 50 Tablet",
                "manufacturer_name": "Unison Pharmaceuticals Pvt Ltd",
                "size": 10,
                "pack_size": "10 Tablets",
                "total_purchase_gst": 5.33,
                "total_net_gst": -0.53,
                "taxable_purchase_amount": 106.67,
                "taxable_sales_amount": 96,
                "profit": -10.67,
                "margin": -11.11
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
    "status_message": "end_date is required",
    "datetime": "2023-01-09 15:07:27",
    "data": null
}
```
{% endtab %}
{% endtabs %}
