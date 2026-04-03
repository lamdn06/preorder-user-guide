---
description: Step 2 of the campaign wizard — configure payment type, deposit amount, and order tags
---

# Payment Settings

## How to set up

From the campaign wizard, navigate to **Step 2: Payment**. Choose how customers pay for their pre-order.

![Step 2 — Payment Type](images/step2-full-framed.png)

{% stepper %}

{% step %}
### Choose payment type

Select one of two payment options:

- **Full payment**: charge the entire product amount when the customer places the pre-order. This is the simplest option — no additional configuration needed.
- **Partial payment (Deposit)**: charge a deposit at checkout and collect the remaining balance later. When selected, additional fields appear (see next steps).
{% endstep %}

{% step %}
### Choose deposit type (when Partial payment is selected)

![Step 2 — Partial payment](images/step2-partial-framed.png)

- **Percentage**: set a percentage of the product price as the deposit.
- **Fixed amount**: set a fixed dollar amount as the deposit.

Toggle between the two options using the **Percentage** / **Fixed amount** buttons.
{% endstep %}

{% step %}
### Set deposit value (when Partial payment is selected)

- **Deposit percentage (%)**: enter the percentage to charge upfront. Example: `20` means the customer pays 20% now.
- **Deposit amount ($)**: enter the fixed amount to charge upfront (shown when "Fixed amount" is selected). Example: `25` means the customer pays $25 regardless of product price.

{% hint style="success" %}
Tip: A 20–30% deposit is a common practice. It secures the customer's commitment while keeping the entry barrier low.
{% endhint %}
{% endstep %}

{% step %}
### Set remaining balance schedule (when Partial payment is selected)

Choose when to collect the remaining payment from the customer:

- **On a specific date**: select a date using the **Charge date** picker. The remaining balance will be charged on that date.
  ◦ Example: `May 01, 2026`
- **Days after checkout**: enter the number of days after the order is placed. The remaining balance is charged automatically.
  ◦ Example: `30` days after checkout

{% hint style="info" %}
The preview panel updates to show the payment message (e.g., "Pay 20% now, 80% later") when partial payment is configured.
{% endhint %}
{% endstep %}

{% step %}
### Add order tags (optional)

Type tag names in the **Tags** search field and press Enter to add them. Tags are automatically added to Shopify orders placed through this campaign.

- Click the **×** on a tag to remove it.
- Example tags: `pre-order`, `summer-2026`, `deposit-paid`

{% hint style="success" %}
Tip: Use tags to filter and manage pre-orders in Shopify Admin. For example, create a smart collection or order view filtered by the `pre-order` tag.
{% endhint %}
{% endstep %}

{% endstepper %}

Click **Continue** to proceed to [Display Settings](display-settings.md), or click **Back** to return to [Campaign Settings](campaign-settings.md).
