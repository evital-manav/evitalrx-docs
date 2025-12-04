# Order Re-Assigned

After placing the order if Order gets rejected by the pharmacy and if there are other Pharmacies available near-by which can fulfill the order then it will be re-assigned to one the pharmacy.

The order might split at re-assignment stage.

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
