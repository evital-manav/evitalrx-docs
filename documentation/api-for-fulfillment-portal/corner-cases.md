# Corner Cases

This document cover the cases which may or may not occur during the order lifecycle and there are some cases which are requested to be taken care by the integration client.

### Checkout V3 Case

* This API provides the real time stock availability cases that can be occur are:
  * Similar to check-serviceability, checkout API is need to be called to have an updated the cart availability as item-availability is directly related to the pharmacy availability directly.
  * On Cart-Screen, Whenever the check-serviceability API is called the checkout should also be called with update `location_token`.

### Place Order Case

* **Price Increase After Order Place:** (very less probability to occur)
  * **Scenario :** While taking the payment if time difference is too large between checkout and place-order due to payment delay(from patient/user) then the `location_token` might change. This might resulting in price-increase.
  * **Solution-1:** Compare the order-total from Place-Order API Response with the payment amount taken from patient(user). If order-total is increased then cancel the order and place a new another.
  * **Solution-2:** Place the order in `pending` state and then take payment on **order-total** from Place-Order Response. And then call **Payment-Webhook  API** to notify us.

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
