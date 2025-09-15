---
description: Some common question that we were asked.
---

# Fulfillment FAQ's

<details>

<summary>Difference Between mrp and price?</summary>

**MRP** is the amount which is printed on product used for selling. While, **price** is the amount we get after applying discount on MRP

</details>

<details>

<summary>Passing prescription URL is mandatory?</summary>

Yes, for medicines where field **is\_rx\_required : "yes" (true)**  it is mandatory to provide prescription. It can be know from the [medicine/view](medicines/view-v3.md) API.

</details>

<details>

<summary>What is Webhook Sequence?</summary>

1. Order Accepted
2. Order Rejected - If not Accepted
3. Order Shipped
4. Order Picked Up
5. Order Split/Reassign

</details>

<details>

<summary>How Rejection Webhook works?</summary>

The Rejection Webhook behavior depends on your onboarding configuration. It can be set up in either of the following ways:

1. **Final Rejection Only** = You’ll receive a webhook once the order is finally rejected.
2. **Each Rejection in Reassignment** = You’ll receive a webhook every time a chemist rejects the order during the reassignment process.

</details>

<details>

<summary>What is use of location_token?</summary>

**location\_token** is calculated at real-time which helps us to ensure accurate serviceability, availability & helps to ensure delivery checks. You can obtain this location token from [here](orders/check-serviceability-v3.md).

</details>

<details>

<summary>What is split &#x26; re-assign, and what is difference between them?</summary>

* Split: This is a configurable option, where split your order to multiple pharmacies in case some of the items are not available at single pharmacy.
* Re-Assign: Generally, when you place order there might be a rare instance when a pharmacy might not accept your order within our time-limit so we re-assing to another pharmacy.

Both of the things are performed by our common webhook [**Order Split/Reassign** ](../api-for-webhook-responses/order-split.md)**.**

</details>

