---
description: To get item details in your inventory by unique medicine Id.
---

# Get Stock details

### <img src="https://static.vecteezy.com/system/resources/thumbnails/018/930/572/small/youtube-logo-youtube-icon-transparent-free-png.png" alt="" data-size="line"> [Before Fetching Stock Details, Add Medicines to Your Inventory](https://youtu.be/v29o6YEsocc?si=WM0nJ2BmAuye7tNE)

### Product Details

<mark style="color:green;">`POST`</mark> [`{{apiUrl}}patient/medicines/get_inventory_status`](https://api.evitalrx.in/v1/patient/medicines/get_inventory_status)

#### Request Body

| Name                                     | Type   | Description                                                                                                                                                                                      |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| apikey<mark style="color:red;">\*</mark> | String | Authentication Token                                                                                                                                                                             |
| medicine\_ids\*                          | String | <p>Stringified Array of medicine_ids.</p><p></p><p>medicine_ids should contain at least 1 medicine_ids.</p><p></p><p>Example:</p><p>["z5s5a+e/Cj4ip7sUl2zJFQ==", "otUfMtG4nIpWSc+oWoX7Lw=="]</p> |

{% tabs %}
{% tab title="200: OK Success" %}
```json
{
  "status_code": "1",
  "status_message": "Success",
  "datetime": "2024-04-25 12:53:46",
  "data": {
    "results": [
      {
        "medicine_id": "TF7Wm49nceLV+NmoM6HJYw==",
        "loose_quantity": 2010,   // quantity at parent chemist or HO
        "strip_quantity": 201,
        "availability": [
          {
            "chemist_id": "qgOgKbBh6UrMJfLyTMtEOw==",
            "chemist_code": "C0065",
            "loose_quantity": 1158,  // quantity at child chemist or Branch
            "strip_quantity": 115
          },
          {
            "chemist_id": "Rzraa93BrrDK9KEVXmPHEQ==",
            "chemist_code": "C0065",
            "loose_quantity": 1160,
            "strip_quantity": 116
          },
          {
            "chemist_id": "M3FvgrgA14Rr2SGTeY7Icw==",
            "chemist_code": "C0065",
            "loose_quantity": 1980,
            "strip_quantity": 198
          },
          {
            "chemist_id": "81PuG89qeGla7moarByvUA==",
            "chemist_code": "C0065",
            "loose_quantity": 1000,
            "strip_quantity": 100
          },
          {
            "chemist_id": "4mtv5aog/Bi0+0q7IsEcRg==",
            "chemist_code": "C0065",
            "loose_quantity": 100,
            "strip_quantity": 10
          }
        ]
      },
      {
        "medicine_id": "iLlokdPAdebp7RYKR5WpnQ==",
        "loose_quantity": 20,
        "strip_quantity": 2,
        "availability": []
      },
      {
        "medicine_id": "M6rdmJ2RYkfkgk+6tEtJmg==",
        "loose_quantity": 1,
        "strip_quantity": 1,
        "availability": []
      }
    ]
  }
}
```
{% endtab %}

{% tab title="200: OK No Product found according to request params" %}
```json
{
    "status_code": "0",
    "status_message": "Invalid medicine key",
    "datetime": "2022-12-06 16:42:59",
    "data": null
}
```
{% endtab %}
{% endtabs %}
