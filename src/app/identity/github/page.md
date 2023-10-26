---
title: Authenticate with GitHub
nextjs:
  metadata:
    title: Authenticate with GitHub
    description: Integrate GitHub OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with GitHub." This tutorial provides step-by-step guidance on setting up GitHub OAuth integration, obtaining a GitHub OAuth App ID and App Secret, configuring the integration in Aikeedo, and enabling "Login with GitHub."
---

Integrate GitHub OAuth 2.0 authentication into your Aikeedo application to offer users the convenience of "Login with GitHub." This tutorial provides step-by-step guidance on setting up GitHub OAuth integration, obtaining a GitHub OAuth App ID and App Secret, configuring the integration in Aikeedo, and enabling "Login with GitHub."

## Prerequisites

Before you start, ensure you have the following:

- A working Aikeedo application.
- A GitHub account for setting up OAuth integration.

## Step 1: Create a GitHub OAuth App

1. **Visit GitHub Developer Settings:**

   - Go to [GitHub Developer Settings](https://github.com/settings/developers).

2. **Create a New OAuth App:**

   - Click on "OAuth Apps" and then select "New OAuth App."

3. **Configure OAuth App Details:**

   - Fill out the required information, including "Application name," "Homepage URL," and "Authorization callback URL." The callback URL should match the one provided by Aikeedo.

4. **Register Application:**

   - Click "Register Application" to create the OAuth App.

5. **OAuth App ID and App Secret:**

   - Note down the "Client ID" and "Client Secret" provided on the OAuth App's settings page. You will need these in the next steps.

## Step 2: Configure Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to GitHub OAuth Settings:**

   - In the admin panel, go to **Settings > Identity Providers > GitHub**.

3. **Enable "Login with GitHub":**

   - Toggle the switch to enable or disable the "Login with GitHub" feature.

4. **Enter GitHub OAuth App ID and App Secret:**

   - Input the "Client ID" and "Client Secret" obtained from your GitHub OAuth App.

5. **Save Changes:**
   - Save your configuration.

## Testing and Usage

With GitHub OAuth integration configured, users will have the option to log in using their GitHub credentials. They can click "Login with GitHub," and the OAuth flow will authenticate and authorize them.

By following these steps, you can seamlessly integrate GitHub OAuth 2.0 into your Aikeedo application. If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
