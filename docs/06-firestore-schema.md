# Firestore Schema

## Version 1 Collections
- users
- customers
- orders
- payments
- adjustments
- expenses
- cash_ledger
- shifts
- closings
- print_logs
- audit_logs
- settings
- summaries

## orders
```text
orderId
displayOrderNo
customerId
customerName
contactNumber
serviceType
status
initialKilo
finalKilo
estimatedLoadCount
finalLoadCount
loads[]
initialPrice
finalPrice
cachedPaidAmount
cachedBalance
paymentStatus
preparedBy
finalizedBy
receivedAt
finalizedAt
processingAt
readyAt
releasedAt
releasedBy
shiftId
notes
createdAt
updatedAt
```

## payments
```text
paymentId
orderId
shiftId
amount
method
paymentType
receivedBy
paidAt
notes
idempotencyKey
```

## adjustments
```text
adjustmentId
orderId
adjustmentType
oldValue
newValue
reason
createdBy
createdAt
correctionOfAdjustmentId
```

## expenses
```text
expenseId
shiftId
category
amount
paymentMethod
description
recordedBy
expenseDate
createdAt
```

## cash_ledger
```text
cashMovementId
shiftId
direction
category
amount
reason
linkedOrderId
linkedExpenseId
recordedBy
recordedAt
```

## shifts
```text
shiftId
openedBy
openedAt
startingCash
status
closedBy
closedAt
```

## closings
```text
closingId
shiftId
expectedCash
actualCash
difference
closingStatus
closingNotes
createdBy
createdAt
```

## summaries
Use one collection with `periodType`, `periodKey`, calculated fields, and `generatedAt`.
