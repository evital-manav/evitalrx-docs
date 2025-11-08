# Order Shipped

In webhook response for `pickup` type order only are `chemist_details` available.

```json
{
  "id": "buctt+C5QzfVvqdIpKkYnQ==",
  "transaction_type": "sales",
  "transaction_nature": "shipped",
  "chemist_id": "9kVNNczng10TbflL7zZEDA==",
  "reference_number": 396,
  "payment_mode": "Cash",
  "payment_date": "2025-01-29 12:19:46",
  "delivery_type": "delivery",
  "order_number": "OOM6HJQ9BT",
  "partner_order_id": "1234",
  "bill_no": 396,
  "bill_date": "2025-01-29 12:26:51",
  "order_status": "shipped",
  "reject_reason": "",
  "total": 1300,
  "amount": 1300,
  "order_by": "Owner",
  "draft_order_id": "y1sw0N315wy4+UDhhT5FjA==",
  "draft_order_shipping_charge": 30,
  "patient_id": "rfojNNab+jNKqxDTYowQSQ==",
  "patient_name": "Manav Patel",
  "mobile": "7458787853",
  "billing_for": "Manav Patel",
  "billing_for_mobile": "7458787853",
  "doctor_name": "",
  "bill-pdf-url": "http://localhost/evital/invoice/T09NNkhKUTlCVA==/print/",
  "invoice_pdf":"https://d2ffmswuyj0h1d.cloudfront.net/storage/invoices/b2c_invoices/OGMDZPAD45.pdf",
  "direct_payment_url": "",
  "remark": "",
  "medicine_refill_reminder_date": "2025-02-05 00:00:00",
  "chemist_code": "C00ER",
  "delivery_person_name": "",
  "delivery_person_mobile": "",
  "chemist_details": {
        "chemist_id": "vUrZeR78iAdoLVZYO6amjA==",
        "pharmacy_name": "Shree Ganesh Pharmacy",
        "pharmacist_name": "Bhumin Patel",
        "contact_no": "7216009775",
        "full_address": "4d SquareVisat, Chennai, Tamil Nadu, India, 380005",
        "latitude": "23.1027599",
        "longitude": "72.5951718",
        "zipcode": "380005",
        "store_timings": {
            "fullday_working": "yes",
            "timings": [
                {
                    "id": "OdONoVbisSnjEbkBi/2lAQ==",
                    "day_of_week": "monday",
                    "working": "yes",
                    "start_time": "10:00:00",
                    "end_time": "19:00:00"
                },
                {
                    "id": "kTJR6KQDmrBy0TqQUoSQug==",
                    "day_of_week": "tuesday",
                    "working": "yes",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "6okjTHgbat0E94JRSSD6hw==",
                    "day_of_week": "wednesday",
                    "working": "yes",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "oNMmkOoRVZgg31i8Sdw/9w==",
                    "day_of_week": "thursday",
                    "working": "yes",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "V52t1Z5PYtC3QKi+v/oDfA==",
                    "day_of_week": "friday",
                    "working": "yes",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "vOKVXLw/5KUiTp3MY2FCuQ==",
                    "day_of_week": "saturday",
                    "working": "yes",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "5qfdG8eHfksSTzjSaMdaHA==",
                    "day_of_week": "sunday",
                    "working": "no",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "2w9ZyrNa+48wl8QmOQOcTw==",
                    "day_of_week": "monday",
                    "working": "yes",
                    "start_time": "08:30:00",
                    "end_time": "14:30:00"
                },
                {
                    "id": "MeYZ1jFOCgmbfr0VloUcHg==",
                    "day_of_week": "tuesday",
                    "working": "yes",
                    "start_time": "07:00:00",
                    "end_time": "13:00:00"
                },
                {
                    "id": "M9F4Aa846tskq8nmCzOI8Q==",
                    "day_of_week": "wednesday",
                    "working": "yes",
                    "start_time": "10:00:00",
                    "end_time": "15:30:00"
                },
                {
                    "id": "cyFsLNErg1nDdEea5Xoaxg==",
                    "day_of_week": "thursday",
                    "working": "yes",
                    "start_time": "08:30:00",
                    "end_time": "14:00:00"
                },
                {
                    "id": "yRzmhhhqdmxYAH2FcsAUcw==",
                    "day_of_week": "friday",
                    "working": "no",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "/VwXyi9uCP//h2/NgYXcnA==",
                    "day_of_week": "saturday",
                    "working": "no",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                },
                {
                    "id": "S+h72C73IChF/cqyP0kQDQ==",
                    "day_of_week": "sunday",
                    "working": "no",
                    "start_time": "00:00:00",
                    "end_time": "23:59:59"
                }
            ]
        }
    },
  "items": [
    {
      "price": 130,
      "directions": "0-0-0-0",
      "quantity": 100,
      "mrp": 130,
      "discount": 0,
      "batch": "ASDAS234",
      "expiry": "02/29",
      "gst": 139.29,
      "gstpercentage": 12,
      "amount": 1300,
      "size": 10,
      "medicine_name": "Dolobest MR 100mg/500mg/250mg Tablet",
      "pack_size": "10 Tablets",
      "dosage_type": "",
      "image": "https://d3cgpvqmlaynvp.cloudfront.net/storage/medicines/thumb/default.jpg",
      "medicine_id": "LXarW6vPNnrbm2bwTZmnOw==",
      "partner_medicine_id": "1234",
      "manufacturer_name": "TTK Healthcare Ltd",
      "hsn_code": "554645",
      "medicine_type": "drug",
      "packing_size": "10 tablets in 1 strip",
      "cess": 0,
      "cess_percentage": 0,
      "price_to_retailer": 75.63,
      "margin": 121.53,
      "base_price": 60.48435,
      "landing_price": 9.011088279625897,
      "location": "",
      "sale_discount": 0,
      "lock_discount": "no",
      "sell_in_loose": "yes",
      "loyalty_points": 0,
      "loyalty_points_percentage": 0,
      "batch_discount": 0,
      "returnable": "yes",
      "b2c_margin": 3,
      "loyalty_points_redeemed": 0,
      "stock_adjusted": "pending",
      "offer_id": 0,
      "item_category": "drug",
      "expiry_return": "2029-02-01",
      "gst_percentage": 12,
      "order_type": "sale",
      "reference_medicine_code": "I00014"
    }
  ],
  "order_custom_fields": {},
  "patient_custom_fields": {}
}
```

