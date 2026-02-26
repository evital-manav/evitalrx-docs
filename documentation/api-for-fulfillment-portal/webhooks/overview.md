---
description: This section contains Fulfillment module webhooks
---

# Overview

Webhooks allow your system to receive **real-time updates** whenever an event occurs in the Fulfillment process. Instead of polling the API, we notify your endpoint with structured event data, enabling seamless integration.

### Webhook Sequence

1. [Digitization Completed](digitization-completed.md) - When the order is Digitized at our PaaS Portal then it is triggered. It is used in [**Order With Prescription Flow**](../orders/place-order.md) & an **Optinal** Webhook.
2. [Order Assigned](order-assigned.md) - When Order is placed and gets asssigned to a pharamacy. This is generally used in Order With Prescription Flow & It is **Optinal** Webhook.
3. [Order Accepted](order-accepted.md) - When order get accepted by pharmacist.
4. [Order Rejected](../../api-for-webhook-responses/order-rejected.md) - If an order is rejected by the pharmacist or order is cancelled manually then this webhook is called.
5. [Order Re-Assign](order-reassigned.md) - When a Order gets Rejected by  Pharmacy we try to re-assign it to another nearby pharmacy.
6. [Order Shipped](order-shipped.md) -  When order is ready for shipping.
   * At this stage the delivery is being assigned to our delivery partner and tracking URL is available. But, it might show no delivery assigned as it will be searching for Delivery Rider.
7. [Order Picked Up](order-picked-up.md) - When order is picked up by delivery rider and details of Delivery rider are available.
8. [Order Delivered](order-delivered.md) - When Order Gets Delivered to patient.
9. [Order Split](order-split.md) ⛔- When order gets reassigned this webhook this triggered.&#x20;
