# Corner Cases

This document cover the cases which may or may not occur during the order lifecycle and there are some cases which are requested to be taken care by the integration client.

### Order Shipped Webhook Case

* **Order Total Amount Decreased,**
  * **Scenario :** At the time of Checkout API we calculate a maximum MRP of each item and then quote the order-total.  But, When the order get assigned the order total might reduce depending upon pharmacy store current item Batch price.
  * **Solution :** The difference between is need to be calculated from Order Shipped webhook or Order View V2 API and need to be handled By integration client.

### Order Return Case

* After Order is Shipped, If patient location is incorrect or patient is not available . Then the order will be Cancelled and Appropriate Reason will be provided within the Order Reject Webhook.
* And If order is returned then there might be penalty for delivery which need to be paid by the clients.

### Order Lost

* In certain cases, after the order has been picked up by the rider, the rider may fraudulently complete the order by obtaining the OTP from the patient without delivering the parcel. OR stole the package.
* Then it will be marked `cancelled` even after it is marked as `completed` .
