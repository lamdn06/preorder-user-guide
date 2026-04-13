---
description: Collect remaining balance from partial payment pre-orders
---

# Collect Payment

## Overview

When a campaign uses **Partial payment**, customers pay a deposit at checkout and the remaining balance is collected later. The **Collect Payment** feature lets you manually trigger payment collection for one or multiple orders at once.

## How to use

### From an order detail

Navigate to **AOV.ai Pre-Order > Reports**, then click on any order number to open the detail page.

![Order detail page](images/order-detail-framed.png)

{% stepper %}

{% step %}
### Review payment summary

The **Payment Summary** sidebar shows the current payment state:

- **Total**: full order amount.
- **Deposit paid**: amount already collected at checkout.
- **Remaining**: outstanding balance due from the customer.
- **Due date**: when the remaining balance is scheduled to be collected.
- **Status**: current payment status (see reference table below).
- **Payment type**: the payment method used (e.g., Partial 20%).
{% endstep %}

{% step %}
### Review payment timeline

The **Payment Timeline** section shows a chronological record of all payment events:

- Order created with total amount
- Deposit paid at checkout
- Remaining balance collected (or collection failed)

Each event includes the date and amount involved.
{% endstep %}

{% step %}
### Collect remaining balance (single order)

When an order has a remaining balance, a **Collect remaining** button appears in the Payment Summary section.

Click **Collect remaining** to open the collection modal:

- The modal shows the exact remaining amount to collect (e.g., "$60.48").
- **Automatically send invoice if charge fails**: enabled by default. If the charge fails, the customer receives an invoice email with a link to pay manually.
- Click **Collect payment** to process.

The app charges the customer's saved payment method via Shopify. On success, the order status updates to **Paid**.

{% hint style="info" %}
The **Collect remaining** button only appears when the order has `Partially paid`, `Failed`, or `Processing` status and has a remaining balance greater than zero.
{% endhint %}
{% endstep %}

{% endstepper %}

### From the order list (bulk collection)

{% stepper %}

{% step %}
### Select orders to collect

From the **Reports** page, use the checkboxes to select one or more orders with outstanding balances.

Click the **Collect payments** button that appears at the top.
{% endstep %}

{% step %}
### Confirm bulk collection

The modal shows how many orders will be processed:

- "You're about to collect the remaining balance from **X** preorder(s)."
- For 50+ orders, a caution message warns that processing may take a few minutes.
- **Automatically send invoice if charge fails**: sends an invoice to customers whose charge fails.

Click **Collect payments** to start processing. A progress bar shows the collection progress.
{% endstep %}

{% step %}
### Review results

After collection completes, a toast notification shows the results:

- **Collected**: number of orders successfully charged.
- **Invoices sent**: number of invoices sent for failed charges.
- **Failed**: number of orders where collection failed.
- **Skipped**: orders that were already paid or had no remaining balance.

{% hint style="success" %}
Tip: After bulk collection, check the **Failed** tab to follow up on orders that couldn't be charged.
{% endhint %}
{% endstep %}

{% endstepper %}

### Payment status reference

| Status | Badge | Meaning |
|--------|-------|---------|
| **Paid** | Green | Full payment received — no action needed |
| **Partially paid** | Orange | Deposit collected, remaining balance outstanding |
| **Processing** | Blue | Payment collection is in progress |
| **Failed** | Red | Payment collection failed — manual follow-up needed |
| **Collected** | Green | Remaining balance successfully collected |

### Invoice fallback

When a charge fails and **Automatically send invoice if charge fails** is enabled:

1. The app sends an invoice email to the customer via Shopify.
2. The customer receives a link to complete payment manually.
3. You can customize the invoice email template in **Shopify Admin > Settings > Notifications**.

{% hint style="info" %}
Invoice emails are sent through Shopify's built-in notification system. The email content and branding follow your Shopify notification settings.
{% endhint %}
