---
layout: post
title: Transactions - Reconcile credit card payments (internal transfers)
date: 2025-10-18 10:00:00 -0000
category: YNAB
---

## Problem
Reconciling two sides of the same transaction (Payment from your checking account to credit card):

## Solution
Create one linked transfer transaction (not two separate income/expense entries) so YNAB treats it as money moving between your own accounts, not spending or income.

### Check that YNAB recognizes them as a transfer
1. Look in the “Payee” column:
2. In your checking account, it should read something like “Transfer: [Credit card name]”
3. In your credit card account, it should read “Transfer: [Checking account name]”
4. If that’s already the case, just approve and reconcile both accounts.

### If they’re not linked automatically
1. Delete one of the duplicate transactions (doesn’t matter which account).
2. Edit the remaining one:
  - In the “Payee” field, choose **Transfer > Credit card** (if you’re editing from the checking account),
  - or **Transfer > Checking** (if editing from the credit card account).
3. YNAB will automatically create the matching entry on the other side.
4. Check that both accounts now show the same transaction, marked as a transfer.

Sometimes YNAB imports them as separate transactions, even with the same amount/date.

## Tip
If you pay your card in full each month, make sure your credit card payment category in YNAB stays green and matches your actual payment. When you transfer funds, YNAB automatically reduces that category and your card balance accordingly — no manual categorizing needed.

### Locate both sides
- In your Checking account register, you should see an outflow, like -$2,000.00, (money leaving your checking).
- In your Credit card account, you’ll see the inflow, like +$2,000.00, (money arriving to pay down the card).
- If YNAB imported both automatically, it may have already linked them.

## Sources
- ChatGPT
- https://support.ynab.com/en_us/transfer-transactions-a-guide-HJOsZz4Jj
