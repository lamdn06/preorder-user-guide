---
description: View, filter, and export pre-order reports
---

# Orders & Reports

## Overview

Navigate to **AOV.ai Pre-Order > Reports** to access the orders management page.

![Orders report page](images/orders-list-framed.png)

## How to use

{% stepper %}

{% step %}
### Review summary metrics

The four cards at the top show a quick snapshot:

- **Total Orders**: total number of pre-orders received.
- **Total Revenue**: combined revenue from all pre-orders.
- **Pending Payment**: orders with outstanding balances (deposit paid, remaining balance due). Shows an "Action needed" badge when count > 0.
- **Fulfilled**: orders that have been shipped or delivered.
{% endstep %}

{% step %}
### Filter orders by status

Use the tab bar to filter:

- **All**: every pre-order regardless of status.
- **Paid**: orders where full payment has been received.
- **Pending Payment**: orders with partial payment — remaining balance is due.
- **Failed**: orders where payment processing failed.
- **Fulfilled**: orders that have been shipped/delivered.
{% endstep %}

{% step %}
### Search for specific orders

Click the **search icon** to find orders by:
- Order number (e.g., `#1020`)
- Customer name
- Customer email
{% endstep %}

{% step %}
### View order details

Click any **order number** to open the detail page:

- **Customer info**: name, email, billing and shipping addresses.
- **Products**: line items with product image, variant, quantity, and price.
- **Payment timeline**: chronological record of all payment events.
- **Payment summary**: deposit amount, remaining balance, total, and payment deadlines.
- **Order metadata**: created date, campaign name, tags, and fulfillment status.

Click **View in Shopify** to open the order in Shopify Admin for fulfillment actions.
{% endstep %}

{% step %}
### Export orders to CSV

1. Select specific orders using the checkboxes on the left, or leave all unselected to export everything.
2. Click **Export CSV** (top right).
3. A CSV file downloads with order details, customer info, payment status, and fulfillment status.

{% hint style="success" %}
Tip: Export "Pending Payment" orders regularly to follow up on outstanding balances.
{% endhint %}
{% endstep %}

{% step %}
### Sync data from Shopify

Click **Sync from Shopify** to pull the latest order updates. Use this when:

- Payment status changed in Shopify (e.g., customer paid remaining balance).
- Fulfillment status was updated in Shopify Admin.
- You suspect pre-order data is out of date.

{% hint style="info" %}
The app automatically syncs orders via webhooks. Manual sync is only needed if you notice stale data.
{% endhint %}
{% endstep %}

{% endstepper %}

### Payment status reference

| Status | Description |
|--------|-------------|
| **Paid** | Full payment received |
| **Partially paid** | Deposit received, remaining balance outstanding |
| **Processing** | Payment is being processed |
| **Failed** | Payment failed |
| **Collected** | Remaining balance has been collected |

### Fulfillment status reference

| Status | Description |
|--------|-------------|
| **Unfulfilled** | Order not yet shipped |
| **On Hold** | Waiting for remaining payment or other action |
| **Scheduled** | Fulfillment scheduled for a future date |
| **In Progress** | Order is being prepared/shipped |
| **Partial** | Some items fulfilled, others pending |
| **Fulfilled** | All items shipped/delivered |
