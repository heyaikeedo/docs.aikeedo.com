---
title: Authenticate with LinkedIn
nextjs:
  metadata:
    title: Authenticate with LinkedIn
    description: Integrate LinkedIn OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with LinkedIn." This tutorial provides step-by-step guidance on setting up LinkedIn OAuth integration, obtaining LinkedIn Client ID and Client Secret, configuring the integration in Aikeedo, and enabling "Login with LinkedIn."
---

Integrate LinkedIn OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with LinkedIn." This tutorial provides step-by-step guidance on setting up LinkedIn OAuth integration, obtaining LinkedIn Client ID and Client Secret, configuring the integration in Aikeedo, and enabling "Login with LinkedIn."

## Prerequisites

Before you start, ensure you have the following:

- A working Aikeedo application.
- A LinkedIn Developer account for setting up OAuth integration.

## Step 1: Create a LinkedIn App

1. **Visit LinkedIn Developer Portal:**

   - Go to [LinkedIn Developer Portal](https://www.linkedin.com/developers/).

2. **Create a New App:**

   - Click on "My Apps" and select "Create App."

3. **Configure App Details:**

   - Fill out the required information such as "App name" and "App logo."

4. **Save and Continue:**

   - Click "Save and Continue" to proceed.

## Step 2: Configure OAuth 2.0 Authentication

1. **Authentication:**

   - In the app dashboard, navigate to the "Authentication" section.

2. **OAuth 2.0 Redirect URLs:**

   - Add the authorized redirect URL provided by Aikeedo. This URL is often click-to-copyable for your convenience.

3. **OAuth 2.0 Client ID and Client Secret:**

   - Note down the "Client ID" and "Client Secret" provided in the "OAuth 2.0 Client ID and Secret" section. You will need these in the next steps.

## Step 3: Configure Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to LinkedIn OAuth Settings:**

   - In the admin panel, go to **Settings > Identity Providers > LinkedIn**.

3. **Enable "Login with LinkedIn":**

   - Toggle the switch to enable or disable the "Login with LinkedIn" feature.

4. **Enter LinkedIn Client ID and Client Secret:**

   - Input the "Client ID" and "Client Secret" obtained from your LinkedIn Developer account.

5. **Save Changes:**
   - Save your configuration.

## Testing and Usage

With LinkedIn OAuth integration configured, users will have the option to log in using their LinkedIn credentials. They can click "Login with LinkedIn," and the OAuth flow will authenticate and authorize them.

By following these steps, you can seamlessly integrate LinkedIn OAuth 2.0 into your Aikeedo application. If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
