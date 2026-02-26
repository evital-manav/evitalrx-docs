# Order Reassigned

When an order gets rejected with `is_final_rejection : false`  then rejected order is re-assigned to a new Pharmacy.

#### Parameter Explanation

* `draft_order_id` : Parent Order ID.
* `rejected_order_id` : Old child order iD.
* `new_order_ids` : Array of New Re-assign Order ID's. (Based on Split Preference Order may or may not get split while reassignment).

```json
{
  "transaction_nature": "reassign",
  "draft_order_id": "EwnAmHOo2VpW9EqocJTMGg==",
  "rejected_order_id": "ItTGXNtpE/G1V53uz89Oyw==",
  "new_order_ids": [
    "FRRVjRuDKiGKcJeOLRBdkg==",
    "4R9SC2ZPX5F2JfWwduff/Q=="
  ]
}
```
