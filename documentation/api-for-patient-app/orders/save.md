---
description: This API is used to Save the draft orders.
---

# Save

## Complete the order.

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in//v1/patient/orders/save`

If the order is made in a draft state, It can be saved by this API. This removes the headache of the integration partners, who don't want their chemists to switch 2 portals. Their portal to place orders, and eVitalRx portal to save the order.

#### Request Body

| Name                                              | Type              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark>     | String            | Id to uniquely identify the patient for whom the order is placed                                                                                                                                                                                                                                                                                                                                                                                           |
| items<mark style="color:red;">\*</mark>           | Stringified Array | <p>List of items with quantity (default in pills). You can change the quantity_type to consider them as strip. </p><p></p><p>All  the params are required shown below. </p><p>Medicine Id and batch should have unique combination. </p><p></p><p><em>i.e.</em> [{ "medicine_id": "vjalpzMV0E33BLwzzLR6fQ==", "batch": "FRESH", "expiry": "2025-12-01", "mrp": 36.1, "quantity": 2, "discount": 0, "gst_percentage": 12, "cess_percentage": 0}]</p><p></p> |
| quantity\_type                                    | strip \| loose    | <p>[strip]: The quantity you are passing will considered as strip </p><p>[loose]: The quantity you are passing will considered as pills</p>                                                                                                                                                                                                                                                                                                                |
| apikey<mark style="color:red;">\*</mark>          | String            | Authentication token                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| patient\_name<mark style="color:red;">\*</mark>   | String            | Name of the Patient                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| shipping                                          | String            | Extra charges in the order.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| delivery\_type                                    | String            | Must be one of **pickup** or **delivery**. default is **pickup.**                                                                                                                                                                                                                                                                                                                                                                                          |
| remark                                            | String            | Note for the Prescription. This param is also available in the Order Details.                                                                                                                                                                                                                                                                                                                                                                              |
| order\_id<mark style="color:red;">\*</mark>       | String            | Order ID from the response of Place Order API.                                                                                                                                                                                                                                                                                                                                                                                                             |
| order\_date<mark style="color:red;">\*</mark>     | String            | <p>Date of the bill. </p><p>Format: YYYY-MM-DD</p><p></p>                                                                                                                                                                                                                                                                                                                                                                                                  |
| parent\_patient\_id                               | String            | If billing for family member, then pass parent patient's ID here.                                                                                                                                                                                                                                                                                                                                                                                          |
| doctor\_id                                        | String            | Encrypted Doctor ID. This ID is available in the Order Details.                                                                                                                                                                                                                                                                                                                                                                                            |
| payment\_status<mark style="color:red;">\*</mark> | Number            | <p>To choose payment mode of the order. </p><p>1: CASH </p><p>2: CREDIT </p><p>3: UPI </p><p>4: CHEQUE </p><p>5: PAYTM </p><p>6: CC/DC </p><p>7: RTGS/NEFT</p>                                                                                                                                                                                                                                                                                             |



{% tabs %}
{% tab title="200: OK Order shipped successfully." %}
```json
{
    "status_code": "1",
    "status_message": "New sales bill created successfully.",
    "datetime": "2023-03-09 17:01:32",
    "ng_version": "0.0.371",
    "data": {
        "order_id": "LcNx52qfdGlw0aHcqmgsRg==",
        "bill_no": "141",
        "order_number": "OKLF112H59",
        "amount": "29",
        "print_url": "http://www.evital.in/invoice/T0tMRjExMkg1OQ==/print/",
        "share_message": "Hi%20Aagam%20Shah%2C%0AThank%20you%20for%20your%20purchase%20at%20*Manav%20Medical%20GJ*.%20We%20hope%20to%20serve%20you%20again.%0AClick%20to%20make%20Payment%20or%20view%20Invoice%3A%20http%3A%2F%2Flocalhost%2Fevital%2Finvoice%2FT0tMRjExMkg1OQ%3D%3D%2F%3Fsource%3DWhatsApp%26medium%3DManual%0A%0AIf%20the%20link%20is%20not%20clickable%2C%20please%20save%20this%20number%20and%20try%20again.%0A%0AYour%20trusted%20pharmacist%2C%0AManav%20Medical%20GJ",
        "invoice_url": "Hi%20Aagam%20Shah%2C%0AThank%20you%20for%20your%20purchase%20at%20*Manav%20Medical%20GJ*.%20We%20hope%20to%20serve%20you%20again.%0AClick%20to%20make%20Payment%20or%20view%20Invoice%3A%20http%3A%2F%2Flocalhost%2Fevital%2Finvoice%2FT0tMRjExMkg1OQ%3D%3D%2F%3Fsource%3DWhatsApp%26medium%3DManual%0A%0AIf%20the%20link%20is%20not%20clickable%2C%20please%20save%20this%20number%20and%20try%20again.%0A%0AYour%20trusted%20pharmacist%2C%0AManav%20Medical%20GJ"
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "order_id is required",
    "datetime": "2023-03-09 17:03:38",
    "data": null
}
```
{% endtab %}
{% endtabs %}
