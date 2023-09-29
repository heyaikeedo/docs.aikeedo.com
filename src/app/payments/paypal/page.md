---
title: How to Enable PayPal Payments
nextjs:
  metadata:
    title: How to Enable PayPal Payments
    description: Unlock the capability to accept secure and convenient payments through PayPal by following these steps.
---

Unlock the capability to accept secure and convenient payments through PayPal by following these steps. {% .lead %}

## Prerequisites

Ensure you have a [PayPal business](https://www.paypal.com/us/business) account before proceeding. Additionally, have your PayPal API secret key, client ID and Webhook Id ready, as these are essential for enabling PayPal recurring payments.

## Get PayPal Rest API secret key and client ID

1. **Log in to Your PayPal Business Account:**

   - Visit [PayPal Developer](https://developer.paypal.com/).
   - Log in with your PayPal business account credentials.

2. **Select Live or Sandbox:**

   - On the Apps & Credentials page, click Live or Sandbox depending on whether you need an app for testing (Sandbox) or going live (Live).

3. **Create a New App:**

   - In the PayPal Developer Dashboard, navigate to [My Apps & Credentials](https://developer.paypal.com/dashboard/applications/sandbox).
   - Click on **Create App** to generate a new app.

4. **Set App details**

   - Enter a name for your app.
   - Select the **Merchant** type.
   - Select Sandbox Account as the **Business Account**.
   - Click on **Create App**.

5. **Retrieve API Keys:**
   - Once the app is created, locate the **Client ID** and **Secret Key** in the app details. Keep these keys secure.

For more information on creating a PayPal app, refer to the [official PayPal documentation](https://www.paypal.com/us/cshelp/article/how-do-i-create-rest-api-credentials-ts1949).

## Get PayPal Webhook ID

Webhooks are necessary for handling recurring payments. Follow these steps to create a webhook and retrieve the webhook ID.

1. **Access Webhooks:**

   - In the PayPal Developer Dashboard, go to **My Apps & Credentials**.
   - Select your app, and under the **Webhooks** section, add a new webhook.

2. **Set Up Webhook Endpoint:**

   - Set the webhook endpoint to `https://yourwebsite.com/webhooks`.

3. **Select Events:**
   - Select all or the following events:
     - `INVOICING.INVOICE.CANCELLED`
     - `INVOICING.INVOICE.CREATED`
     - `INVOICING.INVOICE.PAID`
     - `INVOICING.INVOICE.REFUNDED`
     - `INVOICING.INVOICE.SCHEDULED`
     - `INVOICING.INVOICE.UPDATED`
     - `BILLING.SUBSCRIPTION.CANCELLED`

## Enable PayPal Payments in Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to Payment Settings:**

   - In the admin panel, go to **Settings > Payments > PayPal**.

3. **Enable PayPal Payments:**

   - Set the status to `Enabled` by toggling the switch.
   - Choose between sandbox (for testing) or live mode based on your needs.

4. **Enter API Credentials:**

   - Enter the PayPal API secret key and client ID that you retrieved earlier.

5. **Enter Webhook ID:**

   - Enter the PayPal webhook ID that you retrieved earlier.

6. **Save Changes:**

By completing these steps, you've successfully enabled PayPal payments in Aikeedo. Your users can now securely make payments through PayPal, and the platform is ready to handle recurring payments through webhooks.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:hey@aikeedo.com).
