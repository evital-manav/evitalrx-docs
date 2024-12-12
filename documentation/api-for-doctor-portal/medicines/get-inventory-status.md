---
description: To get status of the items in your inventory.
---

# Get Inventory Status

### <img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Before Fetching Stock Details, Add Medicines to Your Inventory](https://youtu.be/v29o6YEsocc?si=WM0nJ2BmAuye7tNE)

### Inventory Status:

<mark style="color:green;">`POST`</mark>  [`{{apiUrl}}doctor/medicines/get_inventory_status`](https://api.evitalrx.in/v1/doctor/medicines/get_inventory_status)

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                              |
| ---------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication Token                                                                                                                                                                     |
| medicine\_ids                            | String | <p>Stringified Array of medicine_ids.​</p><p></p><p>medicine_ids should contain at least 2 medicine_ids.​ </p><p></p><p>i.e.["z5s5a+e/Cj4ip7sUl2zJFQ==", "otUfMtG4nIpWSc+oWoX7Lw=="]</p> |

{% tabs %}
{% tab title="200: OK Product Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2022-12-08 16:50:09",
    "data": [
        {
            "medicine_id": "otUfMtG4nIpWSc+oWoX7Lw==",
            "chemist_id": "pR/skynRizeVxF1blGRVMw==",
            "quantity": 1380, // Current Quantity
            "mrp": 24,
            "lock_discount": "no", // Default discount if any
            "sell_in_loose": "yes",
            "cess_percentage": 0,
            "gst_percentage": 12
        }
    ]
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid medicine key",
    "datetime": "2022-12-07 11:15:44",
    "data": null
}
```
{% endtab %}
{% endtabs %}
