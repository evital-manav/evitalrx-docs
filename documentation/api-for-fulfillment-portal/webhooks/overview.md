---
description: This section contains Fulfillment module webhooks
---

# Overview

Webhooks allow your system to receive **real-time updates** whenever an event occurs in the Fulfillment process. Instead of polling the API, we notify your endpoint with structured event data, enabling seamless integration.

### Webhook Details

1. [Digitization Completed](digitization-completed.md) - When the order is Digitized at our PaaS Portal then it is triggered. It is used in [**Order With Prescription Flow**](../orders/place-order.md) & an **optional** Webhook.
2. [Digitization Rejected](digitization-rejected.md) - When the Prescription Order is cannot be fulfilled this webhook will be triggered.
3. [Order Assigned](order-assigned.md) - When Order is placed and gets assigned to a pharmacy. This is generally used in Order With Prescription Flow & It is **optional** Webhook.
4. [Order Accepted](order-accepted.md) - When order get accepted by pharmacist.
5. [Order Rejected](../../api-for-webhook-responses/order-rejected.md) - If an order is rejected by the pharmacist or order is cancelled manually then this webhook is called.
6. [Order Re-Assign](order-reassigned.md) - When a Order gets Rejected by  Pharmacy we try to re-assign it to another nearby pharmacy.
7. [Order Shipped](order-shipped.md) -  When order is ready for shipping.
   * At this stage the delivery is being assigned to our delivery partner and tracking URL is available. But, it might show no delivery assigned as it will be searching for Delivery Rider.
8. [Order Picked Up](order-picked-up.md) - When order is picked up by delivery rider and details of Delivery rider are available.
9. [Order Delivered](order-delivered.md) - When Order Gets Delivered to patient.
10. [Order Split](order-split.md) ⛔- When order gets reassigned this webhook this triggered.&#x20;



### Webhook Sequence

#### Delivery Order Sequence

1. Digitization Completed. _(Only Prescription Order)_
2. Digitization Rejected. _(Only Prescription Order)_
3. Order Assigned. (Optional)
4. Order Accepted.
5. Order Rejected.
6. Order Re-Assign. _(If Order gets Re-assigned)_
7. Order Shipped
8. Order Picked Up
9. Order Delivered

#### Pickup Order Sequence

1. Order Accepted.
2. Order Rejected.
3. Order Shipped
4. Order Delivered
