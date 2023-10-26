---
title: Authenticate with Facebook
nextjs:
  metadata:
    title: Authenticate with Facebook
    description: Integrate Facebook OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with Facebook." This tutorial provides step-by-step guidance on setting up Facebook OAuth integration, obtaining a Facebook App ID and App Secret, configuring the integration in Aikeedo, and enabling "Login with Facebook."
---

Integrate Facebook OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with Facebook." This tutorial provides step-by-step guidance on setting up Facebook OAuth integration, obtaining a Facebook App ID and App Secret, configuring the integration in Aikeedo, and enabling "Login with Facebook."

## Prerequisites

Before you start, ensure you have the following:

- A working Aikeedo application.
- A Facebook Developer account for setting up OAuth integration.

## Step 1: Create a Facebook App

1. **Visit Facebook for Developers:**

   - Go to [Facebook for Developers](https://developers.facebook.com/).

2. **Create a New App:**

   - Click on "My Apps" and select "Create App."

3. **Select a Platform:**
   - Choose the platform that aligns with your application, e.g., "Website."

## Step 2: Configure Basic Settings

1. **App Details:**

   - Enter the "Display Name" and "Contact Email."

2. **Add a Platform:**

   - Scroll down to the "Add a Platform" section and select "Website."

3. **Enter Site URL:**

   - In the "Site URL" field, enter the URL of your Aikeedo application.

4. **Save Changes:**
   - Click "Save Changes."

## Step 3: Obtain Facebook App ID and App Secret

1. **App Dashboard:**

   - In your Facebook Developer account, go to the app dashboard for the newly created app.

2. **App ID and App Secret:**
   - Note down the "App ID" and "App Secret" located in the "App Secret" section. You will need these in the next steps.

## Step 4: Configure Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to Facebook OAuth Settings:**

   - In the admin panel, go to **Settings > Identity Providers > Facebook**.

3. **Enable "Login with Facebook":**

   - Toggle the switch to enable or disable the "Login with Facebook" feature.

4. **Enter Facebook App ID and App Secret:**

   - Input the "App ID" and "App Secret" obtained from your Facebook Developer account.

5. **Save Changes:**
   - Save your configuration.

## Testing and Usage

With Facebook OAuth integration configured, users will have the option to log in using their Facebook credentials. They can click "Login with Facebook," and the OAuth flow will authenticate and authorize them.

By following these steps, you can seamlessly integrate Facebook OAuth 2.0 into your Aikeedo application.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
