---
description: Step 3 of the campaign wizard — customize the pre-order button, badge, and messages on your storefront
---

# Display Settings

## How to set up

From the campaign wizard, navigate to **Step 3: Display setting**. Customize how the pre-order experience looks on your storefront.

![Step 3 — Button and Badge](images/step3-top-framed.png)

{% stepper %}

{% step %}
### Set button text

- **Button text**: the label displayed on the pre-order button that replaces "Add to Cart." Default: `Pre-Order Now`
  ◦ Other examples: `Reserve Now`, `Get it First`, `Pre-Order`
{% endstep %}

{% step %}
### Choose button colors

- **Background color**: the fill color of the button. Click the color swatch to open the picker. Default: `#1A1A1A` (dark)
- **Text color**: the color of the button label. Default: `#FFFFFF` (white)

{% hint style="success" %}
Tip: Match the button colors to your store theme for a cohesive look.
{% endhint %}
{% endstep %}

{% step %}
### Enable Pre-Order badge

Check or uncheck the **Pre-Order Badge** checkbox to show or hide the badge on product cards in collection pages and search results. Default: Enabled.

When enabled, configure:
- **Badge text**: the text displayed on the badge. Default: `Pre-Order`
{% endstep %}

{% step %}
### Choose badge colors

- **Background color**: badge fill color. Default: `#E53E3E` (red)
- **Text color**: badge text color. Default: `#FFFFFF` (white)

{% hint style="info" %}
The badge is only visible when the app embed is activated in your theme. Go to **Online Store > Themes > Customize > App embeds** and enable **AOV.ai Pre-Order**.
{% endhint %}
{% endstep %}

{% step %}
### Edit delivery message

![Step 3 — Custom Messages](images/step3-messages-framed.png)

- **Delivery message**: shown below the pre-order button on the product page.
  ◦ Default: `Estimated delivery: {{delivery_date}}`
  ◦ Supported variables: `{{delivery_date}}`, `{{product_title}}`
{% endstep %}

{% step %}
### Edit payment message

- **Payment message**: shown when partial payment is enabled, indicating deposit terms.
  ◦ Default: `Pay {{deposit_amount}} now, {{remaining_amount}} later`
  ◦ Supported variables: `{{deposit_amount}}`, `{{remaining_amount}}`, `{{charge_date}}`
{% endstep %}

{% step %}
### Edit cart messages

- **Cart message label**: the label shown on the left side of cart properties. Default: `Delivery`
- **Cart message**: the message shown in the cart for pre-order line items. Default: `This is a pre-order item. {{delivery_date}}`
  ◦ Supported variables: `{{delivery_date}}`, `{{deposit_amount}}`

{% hint style="success" %}
Tip: Variables like `{{delivery_date}}` are automatically replaced with actual values. They are preserved across all languages when using translations.
{% endhint %}
{% endstep %}

{% step %}
### Preview and save

Use the **Preview** panel (right side) to verify your settings. Switch between:

- **Product Page**: button with custom text/colors, badge, delivery message, payment message.
- **Collection**: product card with badge overlay.
- **Cart**: cart line item with delivery note.

When everything looks good, click **Save changes** to activate your campaign.

{% hint style="warning" %}
After saving, make sure the app embed is activated in your Shopify theme. Go to **Online Store > Themes > Customize > App embeds** and enable **AOV.ai Pre-Order**.
{% endhint %}
{% endstep %}

{% endstepper %}

### Supported variables reference

| Variable | Where used | Description | Example output |
|----------|-----------|-------------|----------------|
| `{{delivery_date}}` | Delivery message, Cart message | Delivery date from Step 1 | `10/04/2026` |
| `{{product_title}}` | Delivery message | Product name | `Summer Dress` |
| `{{deposit_amount}}` | Payment message, Cart message | Deposit amount | `$20.00` or `20%` |
| `{{remaining_amount}}` | Payment message | Remaining balance | `$80.00` or `80%` |
| `{{charge_date}}` | Payment message | Date remaining balance is due | `05/01/2026` |

Click **Back** to return to [Payment Settings](payment-settings.md).
