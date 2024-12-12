---
description: To add patients with mobile number, name and address.
---

# Add / Update Customer

## Add Patient &#x20;

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}b2b/add_update_pharmacy`](https://api.evitalrx.in/v1/b2b/add_update_pharmacy)

#### Request Body

| Name                                             | Type   | Description                                                                                                                                                        |
| ------------------------------------------------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| pharmacy\_name<mark style="color:red;">\*</mark> | String | Name of the pharmacy                                                                                                                                               |
| mobile<mark style="color:red;">\*</mark>         | Number | Mobile number of pharmacy                                                                                                                                          |
| address<mark style="color:red;">\*</mark>        | String | Address of the pharmacy                                                                                                                                            |
| apikey<mark style="color:red;">\*</mark>         | String | Authentication token                                                                                                                                               |
| id                                               | Number | <p>Unique ID of address, If provided, it will update the address associated with this ID.</p><p>If this ID is not provided, then new address will be inserted.</p> |
| pharmacist\_name                                 | String | Name of the Pharmacist                                                                                                                                             |
| gstn\_number                                     | String | The GSTN Number of the pharmacy                                                                                                                                    |
| pan\_no                                          | String | The PAN Number of the pharmacy                                                                                                                                     |
| discount\_percentage                             | Number | Default discount percentage for the pharmacy                                                                                                                       |
| license\_number\_20                              | String | Drug License of pharmacy                                                                                                                                           |
| license\_number\_21                              | String | Wholesale License of pharmacy                                                                                                                                      |
| address\_line2                                   | String | Street or Landmark of the pharmacy address                                                                                                                         |
| email                                            | String | Email of the pharmacy                                                                                                                                              |
| area                                             | String | The area where the pharmacy is located                                                                                                                             |
| phone                                            | String | The phone number of the pharmacy                                                                                                                                   |
| entity\_type                                     | String | The type of entity; must be one of 'chemist', 'doctor', or 'b2b\_customer' defaults to 'chemist'                                                                   |



{% tabs %}
{% tab title="200 Patient added successfully." %}
```json
{
    "status_code": "1",
    "status_message": "New Pharmacy Added Successfully",
    "datetime": "2024-10-01 15:56:54",
    "data": {
        "chemist_id": "kg/N9s0A0Y03GXuiuo/Iqw==", // ID of newly added/existing B2B Chemist/Customer
        "pharmacy_name": "Sharma Medical Store",
        "pharmacist_name": "Sdsadasdsd",
        "mobile": "1414141414",
        "gstn_number": "10AKEPK5905A1ZZ",
        "pan_no": "4445454588",
        "area": "Motera",
        "city": ""
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Please enter valid GSTIN format",
    "datetime": "2024-10-01 15:58:41",
    "data": null
}
```
{% endtab %}
{% endtabs %}

