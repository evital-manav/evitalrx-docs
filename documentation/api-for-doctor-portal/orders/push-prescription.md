---
description: To push prescription with items and its quantity.
---

# Push Prescription

## Push Prescription

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/orders/push_prescription`

#### Request Body

| Name                                          | Type   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| patient\_id<mark style="color:red;">\*</mark> | String | <p>Id to uniquely identify the patient for whom the order is placed. </p><p></p><p>Pass blank ('') if mobile and patient_name is passed in the request body. it will automatically create the patient.</p>                                                                                                                                                                                                                                                        |
| items<mark style="color:red;">\*</mark>       | Array  | <p>List of items with quantity (in pills) and medicine_id and discount_percentage. Max 99% discount is allowed.</p><p></p><p>dosage details can be passed through directions in 1-1-1-1 (morning-noon-evening-night) format. </p><p></p><p>Not required, if Prescription is Passed in the <strong>image</strong> param. </p><p></p><p>i.e. [{ "medicine_id":"haaLvntZX7KmadCtJa314w==", "quantity":10, "discount_percentage": 5, "directions": "0-1-0.5-2" }]</p> |
| image                                         | File   | Image of the prescription, if provided items will not be required.                                                                                                                                                                                                                                                                                                                                                                                                |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| patient\_name                                 | String | <p>Name of the Patient. </p><p></p><p>Only required if patient_id is passed blank. </p>                                                                                                                                                                                                                                                                                                                                                                           |
| doctor\_name                                  | String | <p>Name of the Prescribing doctor <br></p>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| batch\_with                                   | String | <p>Must be <strong>yes</strong> or <strong>no</strong><br><strong>yes</strong> will Auto feed the batches based on the shortest expiry &#x26; stock availability<br><strong>no</strong> will keep the batch details empty</p>                                                                                                                                                                                                                                     |
| delivery\_type                                | String | Must be one of **pickup** or **delivery**.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| remark                                        | String | Note for the Prescription.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| parent\_patient\_id                           | String | If billing for family member, then pass parent patient's ID here.                                                                                                                                                                                                                                                                                                                                                                                                 |
| shipping                                      | Number | Delivery or Extra charges to be added in the order. default: 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| mobile                                        | String | <p>Mobile of the Patient. </p><p></p><p>Only required if patient_id is passed blank. </p>                                                                                                                                                                                                                                                                                                                                                                         |
| custom\_fields                                | Object | <p>Key value pairs of custom attribute key and it's value.<br>For ex: <br>{"prescription_id": "879", "appointment_id": "123"}</p>                                                                                                                                                                                                                                                                                                                                 |
| order\_action                                 | string | possible value : merge,update,""                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| order\_id                                     | string | <p>1.When you want to merge a prescription, you need to pass the order_id to which you want to merge.<br>And order_action should be "merge".<br><br>2.When you want to update a prescription, you need to pass the order_id to which you want to update.<br><br><br></p>                                                                                                                                                                                          |

{% tabs %}
{% tab title="200: OK Order Placed successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Order placed successfully",
    "datetime": "2022-12-07 14:18:11",
    "data": {
        "order_id": "jcdPUtlOBIBZY6xfDXJ6Gw==",
        "order_number": "ODLBDER3UQ"
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Patient Key",
    "datetime": "2022-12-07 14:18:44",
    "data": null
}
```
{% endtab %}
{% endtabs %}
