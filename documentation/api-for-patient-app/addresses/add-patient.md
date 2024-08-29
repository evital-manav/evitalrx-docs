# List Addresses

## &#x20;&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/patient/addresses`

#### Request Body

| Name                                          | Type   | Description          |
| --------------------------------------------- | ------ | -------------------- |
| apikey<mark style="color:red;">\*</mark>      | String | Authentication token |
| patient\_id<mark style="color:red;">\*</mark> | String | Unique ID of patient |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-10-31 10:56:17",
    "data": {
        "results": [
            {
                "id": "1NaBJ+MBG9iGjRzCHAMQkA==",
                "address_name": "home",
                "address": "Kurubarahalli",
                "address_line2": "Bengaluru, Karnataka 562162",
                "city": "Bangalore",
                "state": "Karnataka",
                "country": "India",
                "zipcode": "562130",
                "latitude": "13.002850494898789",
                "longitude": "77.52918554865722",
                "is_default": "yes",
                "created_date": "2023-07-24 16:02:03",
                "updated_date": "2023-09-18 17:53:16"
            },
            {
                "id": "N2RmoMcZ4KBD61jT06Tc9w==",
                "address_name": "home",
                "address": "Cambridge Road",
                "address_line2": "Halasuru",
                "city": "Bangalore",
                "state": "Karnataka",
                "country": "India",
                "zipcode": "560008",
                "latitude": "12.9715979",
                "longitude": "77.6275356",
                "is_default": "no",
                "created_date": "2023-08-25 15:59:22",
                "updated_date": "2023-09-18 17:52:27"
            },
            {
                "id": "76M0+Kteb7onM2/zAPnnSg==",
                "address_name": "home",
                "address": "C-32, Pushpak City",
                "address_line2": "Hathijan",
                "city": "Ahmedabad",
                "state": "Gujarat",
                "country": "India",
                "zipcode": "382445",
                "latitude": "22.95148617583943",
                "longitude": "72.66486683544312",
                "is_default": "no",
                "created_date": "2023-01-11 18:30:49",
                "updated_date": "2023-09-18 17:54:19"
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
    "status_message": "Invalid Patient Key",
    "datetime": "2023-10-31 10:57:03",
    "data": null
}
```
{% endtab %}
{% endtabs %}

