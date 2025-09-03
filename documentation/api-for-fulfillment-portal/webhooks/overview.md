---
description: This section contains Fulfillment module webhooks
---

# Overview

Webhooks allow your system to receive **real-time updates** whenever an event occurs in the Fulfillment process. Instead of polling the API, we notify your endpoint with structured event data, enabling seamless integration.

### Webhook Sequence

1. [Order Accepted](../../api-for-webhook-responses/order-accepted.md) - When order get accepted by pharmacist.
2. [Order Rejected](../../api-for-webhook-responses/order-rejected.md) - If an order is rejected by the pharmacist, the webhook will be triggered according to the client’s configuration specified during onboarding.
   * **Final Rejection**:
     * Webhook is received only once after the order cannot be fulfilled in multiple reassignments.
   * **Each Rejection**:
     * Webhook is sent each time a pharmacy rejects the order during the reassignment process until the final rejection.
3. [Order Shipped](../../api-for-webhook-responses/order-shipped.md) -  When order is ready for shipping.
   * At this stage the delivery is being assigned to our delivery partner and tracking URL is available. But, it might show no delivery assigned as it will be searching for Delivery Rider.
4. [Order Picked Up](../../api-for-webhook-responses/order-picked-up.md) - When order is picked up by delivery rider and details of Delivery rider are available.
5. [Order Delivered](../../api-for-webhook-responses/order-delivered.md) - When Order Gets Delivered to patient.
6. [Order Split](../../api-for-webhook-responses/order-split.md) - When order split into multiple orders.
