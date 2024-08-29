---
description: To search content
---

# Search Content

## Search Contents

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/catalog/medicines/content_search`

#### Request Body

| Name                                      | Type   | Description             |
| ----------------------------------------- | ------ | ----------------------- |
| content<mark style="color:red;">\*</mark> | String | Content to be searched. |
| apikey<mark style="color:red;">\*</mark>  | String | Authentication token    |

{% tabs %}
{% tab title="200 Products Retrieved Successfully" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-05-15 18:54:34",
    "data": {
        "results": [
            {
                "content": "Paradichlorobenzene (4gm)",
                "id": "TmOVsxtb5BlFs4px88ReRQ=="
            },
            {
                "content": "Paradichlorobenzene (162.5mg)",
                "id": "c7OJPXkeXCg/8pa130GbTg=="
            },
            {
                "content": "Paradichlorobenzene (320mg)",
                "id": "VcelI1X0zp2urnxD6sbnJw=="
            },
            {
                "content": "Propyl Paraben (180mcg)",
                "id": "vY/1wcav8EcVHA0otFK67Q=="
            },
            {
                "content": "Propyl Paraben (850.0mg)",
                "id": "0K50lD2ZYe6ZCitNDtfJZQ=="
            },
            {
                "content": "Paradichlorobenzene (0.38%w/w)",
                "id": "+Du4PAgn4slRMnpBsqaYPw=="
            },
            {
                "content": "Para Amino Benzoic Acid (500mg)",
                "id": "Ez+RTplCJoRJpyEHzxaAPQ=="
            },
            {
                "content": "Propyl Paraben (1.5gm)",
                "id": "6UPouwJuJnDVRDEHz5Zjyw=="
            },
            {
                "content": "Propyl Paraben (600000iu)",
                "id": "TRTCy6rIpJjr3JprQmITZA=="
            },
            {
                "content": "Propyl Paraben (0.31mg)",
                "id": "I3XKPhvcLdUgojwrUhlMuw=="
            }
        ]
    }
}
```
{% endtab %}

{% tab title="200: OK No Products found" %}
```json
{
    "status_code": "1",
    "status_message": "Success",
    "datetime": "2023-05-15 18:54:46",
    "data": {
        "results": []
    }
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "content is required",
    "datetime": "2023-05-15 18:54:59",
    "data": null
}
```
{% endtab %}
{% endtabs %}

