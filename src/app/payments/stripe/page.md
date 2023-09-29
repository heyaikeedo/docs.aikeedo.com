---
title: How to Enable Stripe Payments
nextjs:
  metadata:
    title: How to Enable Stripe Payments
    description: Empower your Aikeedo platform to accept seamless and secure payments through Stripe by following these straightforward steps.
---

Empower your Aikeedo platform to accept seamless and secure payments through Stripe by following these straightforward steps. {% .lead %}

## Prerequisites

Ensure you have a [Stripe](https://stripe.com/) account before proceeding. Additionally, have your Stripe API secret key and publishable key ready, and webhook secret, as these are essential for enabling Stripe payments.

## Get Stripe API Keys

1. **Log in to Your Stripe Account:**

   - Visit [Stripe Dashboard](https://dashboard.stripe.com/).
   - Log in with your Stripe account credentials.

2. **Access API Keys:**

   - In the Dashboard, navigate to **Developers > API keys**.
   - Retrieve your **Secret Key** and **Publishable Key**. Keep these keys secure.

For more information on obtaining Stripe API keys, refer to the [official Stripe documentation](https://stripe.com/docs/keys).

## Get Stripe Webhook Secret

Webhooks are necessary for handling recurring payments. Follow these steps to create a webhook and retrieve the webhook secret.

1. **Access Webhooks:**

   - In the Stripe Dashboard, go to **Developers > Webhooks**.
   - Click on **Add endpoint**.

2. **Set Up Webhook Endpoint:**

   - Set the webhook endpoint to `https://yourwebsite.com/webhooks`.

3. **Select Events:**

   - Select all or the following events:
     - `invoice.created`
     - `invoice.updated`
     - `invoice.finalized`
     - `invoice.marked_uncollectible`
     - `invoice.payment_succeeded`
     - `invoice.deleted`
     - `invoice.voided`
     - `customer.subscription_updated`
     - `customer.subscription_deleted`

## Enable Stripe Payments in Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to Payment Settings:**

   - In the admin panel, go to **Settings > Payments > Stripe**.

3. **Enable Stripe Payments:**

   - Set the status to `Enabled` by toggling the switch.
   - Choose between test (for testing) or live mode based on your needs.

4. **Enter API Credentials:**

   - Enter the Stripe API secret key and publishable key, and webhook secret that you retrieved earlier.

5. **Save Changes:**

By completing these steps, you've successfully enabled Stripe payments in Aikeedo. Your users can now make secure payments through Stripe, ensuring a smooth and reliable transaction process.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:hey@aikeedo.com).
