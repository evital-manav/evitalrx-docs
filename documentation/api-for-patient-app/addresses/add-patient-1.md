# Add-Update Address

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/addresses/add_update`](https://api.evitalrx.in/v1/patient/addresses/add_update)

#### Request Body

| Name                                            | Type   | Description                                                                                                                                                                 |
| ----------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>        | String | Authentication token                                                                                                                                                        |
| patient\_id<mark style="color:red;">\*</mark>   | String | Unique ID of patient                                                                                                                                                        |
| address\_name<mark style="color:red;">\*</mark> | String | <p>Valid Values: "home" | "work" </p><p></p><p>Address type</p><p></p>                                                                                                      |
| address\_id                                     | String | <p>Unique ID of address, If provided, it will update the address associated with this ID. </p><p></p><p>If this ID is not provided, then new address will be inserted. </p> |
| address<mark style="color:red;">\*</mark>       | String | Address of the patient                                                                                                                                                      |
| address\_line2                                  | String | Area, street or Landmark of the patient address.                                                                                                                            |
| city                                            | String | City of the patient                                                                                                                                                         |
| state                                           | String | State of the patient                                                                                                                                                        |
| zipcode                                         | String | Pincode of the patient's address.                                                                                                                                           |
| latitude                                        | Number | GPS co-ordinate of the patient's address.                                                                                                                                   |
| longitude                                       | Number | GPS co-ordinate of the patient's address.                                                                                                                                   |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Address updated successfully",
    "datetime": "2023-10-31 11:50:05",
    "data": {
        "address_name": "home",
        "address": "Kurubarahalli",
        "address_line2": "Bengaluru, Karnataka 562162",
        "city": "Bangalore",
        "state": "Karnataka",
        "country": "India",
        "zipcode": "562130",
        "latitude": "11",
        "longitude": "72",
        "is_default": "no",
        "id": "r6ISwkWxJLDDhxprrJ0D8w==" // Unique Address ID
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid Patient Key",
    "datetime": "2023-10-31 10:57:03",
    "data": null
}
```
{% endtab %}
{% endtabs %}

