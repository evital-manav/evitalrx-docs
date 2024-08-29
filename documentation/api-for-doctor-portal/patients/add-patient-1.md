---
description: To add family member of the patient
---

# Add Patient family member

## &#x20;&#x20;

<mark style="color:green;">`POST`</mark> `https://api.evitalrx.in/v1/doctor/patients/add_family_member`

#### Request Body

| Name                                                      | Type   | Description                                                                                                                                                                                                                            |
| --------------------------------------------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| apikey<mark style="color:red;">\*</mark>                  | String | Authentication token                                                                                                                                                                                                                   |
| mobile                                                    | Number | Mobile number of Patient's family member                                                                                                                                                                                               |
| first\_name<mark style="color:red;">\*</mark>             | String | First name of Patient's family member                                                                                                                                                                                                  |
| last\_name<mark style="color:red;">\*</mark>              | String | Last name of Patient's family member                                                                                                                                                                                                   |
| dob<mark style="color:red;">\*</mark>                     | String | <p>Date of Birth of the Patient</p><p>Format: YYYY-MM-DD</p>                                                                                                                                                                           |
| patient\_id<mark style="color:red;">\*</mark>             | String | Key of the Patient whose family member is going to be added.                                                                                                                                                                           |
| blood\_group                                              | String | Blood Group of the Patient                                                                                                                                                                                                             |
| relation<mark style="color:red;">\*</mark>                | String | <p>Relation with the Parent Patient. Possible values are: </p><p>[ "Brother", "Sister", "Father", "Mother", "Son", "Daughter", "Grand_Father", "Grand_Mother", "Uncle", "Aunt", "Wife", "Husband", "Grand_Daughter", "Grand_Son" ]</p> |
| parent\_patient\_mobile<mark style="color:red;">\*</mark> | String | Either pass the Parent patient's Mobile Or Patient ID                                                                                                                                                                                  |

{% tabs %}
{% tab title="200 Patient added successfully." %}
```
{
    "status_code": "1",
    "status_message": "Family member added successfully",
    "datetime": "2022-12-23 11:36:23",
    "data": {
        "relation": "Brother",
        "firstname": "Manav",
        "lastname": "Chauhan",
        "mobile": "",
        "patient_family_member_id": "jtyjX7EP2GPrTdF+bFGBww==",
        "blood_group": "B+",
        "dob": "2001-10-14",
        "id": "m3nc908treoPV7VLHehTAA==",
        "profile_picture": ""
    }
}
```
{% endtab %}

{% tab title="200: OK Patient added Failed" %}
```
{
    "status_code": "0",
    "status_message": "This mobile number is already exist as a patient",
    "datetime": "2022-12-23 11:39:53",
    "data": {}
}
```
{% endtab %}

{% tab title="200: OK Validation Error" %}
```json
{
    "status_code": "0",
    "status_message": "\"first_name\" is required",
    "datetime": "2022-12-23 11:40:24",
    "data": null
}
```
{% endtab %}
{% endtabs %}

