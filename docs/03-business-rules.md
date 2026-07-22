# Business Rules

## Initial and Final Values
Initial values must never be silently overwritten.

Preserve:
- initial kilo
- final kilo
- initial price
- final price
- estimated load count, if provided
- final load count
- final load classifications

## Laundry Checking Process
After the laundry is opened, checked, and segregated, staff may discover towels, bedsheets, comforters, or other items that change kilo, load count, classification, and price.

Any change must create an append-only adjustment record with reason, user, and timestamp.

## Load Classifications
- SMALL_LOAD
- LIGHT
- HEAVY
- MIXED
- BEDSHEET_COMFORTER

Every final load must have exactly one classification.

## Payment Status
- NP
- PARTIAL
- PAID
- BALANCE_DUE

## Payment Method
- CASH
- GCASH
- BANK
- OTHER

Payment status and payment method are separate.

## Release Rule
Laundry cannot be released while balance is greater than zero unless an authorized override is recorded.

## Cash Rules
- Cash payments affect physical cash
- Digital payments do not increase physical cash
- Owner withdrawals reduce cash but are not business expenses
- Closed shifts are immutable without controlled correction

## Shift Closing Formula
```text
Expected Cash =
Starting Cash
+ Cash Payments
+ Other Cash In
- Cash Out
- Cash Expenses
- Refunds
- Owner Withdrawals
```

```text
Difference = Actual Cash - Expected Cash
```
