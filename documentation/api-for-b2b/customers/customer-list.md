---
description: To get the patient details
---

# Customer List

## Get Patient

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/b2b/b2b_customers`

#### Request Body

| Name                                     | Type   | Description                                                                                           |
| ---------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark> | String | Authentication token                                                                                  |
| searchstring                             | String | <p>Min: 3 char required, accepts:<br>1. pharmacy name<br>2.mobile number<br>3. area</p>               |
| orderby                                  | String | <p>Field to order results by, accepts:<br>1. pharmacy_name  (default)<br>2. net_credit<br>3. area</p> |
| order                                    | String | <p>Order direction, accepts:<br>1. asc (default)<br>2. desc</p>                                       |



{% tabs %}
{% tab title="200 Patient details retrieved successfully." %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2024-10-01 17:47:32",
    "data": {
        "current_page": 1,
        "rpp": 20,
        "results": [
            {
                "net_credit": 0,
                "chemist_name": "Milton Pharmacy",
                "customer_attributes_mobile": "8888885559",
                "pharmacy_name": "Milton Pharmacy",
                "mobile": "8888885559",
                "buyer_chemist_id": "T8JDTcqL4yfys2dMdww02A==",
                "area": "Motera",
                "state": "Gujarat",
                "country": "India",
                "zipcode": "380005",
                "city": "Ahmedabad",
                "status": "active"
            },
            {
                "net_credit": 0,
                "chemist_name": "Doe Pharmacy",
                "customer_attributes_mobile": "8564213978",
                "pharmacy_name": "Doe Pharmacy",
                "mobile": "8564213978",
                "buyer_chemist_id": "NwwR8+AEqAAr8JXDyAeqYQ==",
                "area": "",
                "state": "Karnataka",
                "country": "India",
                "zipcode": "560025",
                "city": "Bangalore",
                "status": "active"
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
    "status_message": "order must be one of [asc, desc]",
    "datetime": "2024-10-01 17:48:32",
    "data": null
}
```
{% endtab %}
{% endtabs %}

