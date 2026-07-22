# Workflows

## Main Laundry Workflow
```text
Bagong Laundry
→ Save Order
→ Print Customer Claim Stub
→ Print Laundry Tag
→ Naghihintay
→ Ayusin ang Labada
→ Confirm Final Kilo
→ Confirm Final Load Count
→ Assign Load Classifications
→ Confirm Final Price
→ Isalang
→ Nilalabhan
→ Ready for Pickup
→ Search in Kukunin
→ Collect Remaining Payment
→ Print Final Receipt
→ Release Laundry
```

## New Laundry
Capture customer name, contact, service, initial kilo, initial price, payment status, payment method if needed, prepared by, and notes.

Do not require final load details here.

## Ayusin ang Labada
Capture final kilo, final load count, classification per load, final price, reason for changes, finalized by, and timestamp.

## Pickup
Search by order ID, customer name, or contact number. Check balance before release.

## Cancel / Void
No silent deletion. Always record reason, user, timestamp, and approval if required.
