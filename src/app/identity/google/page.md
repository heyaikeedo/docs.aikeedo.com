---
title: Authenticate with Google
nextjs:
  metadata:
    title: Authenticate with Google
    description: Integrate Google OAuth 2.0 authentication into your Aikeedo application to provide users with the convenient "Login with Google" option. This tutorial will guide you through the setup process, including obtaining a Google Client ID and secret key, configuring the integration, and enabling the "Login with Google" feature.
---

Integrate Google OAuth 2.0 authentication into your Aikeedo application to provide users with the convenient "Login with Google" option. This tutorial will guide you through the setup process, including obtaining a Google Client ID and secret key, configuring the integration, and enabling the "Login with Google" feature.

## Prerequisites

Before you begin, ensure you have the following:

- Aikeedo application installed and accessible.
- Google account for setting up OAuth integration.

## Step 1: Create a Google API Project

1. **Visit Google Cloud Console:**

   - Go to [Google Cloud Console](https://console.cloud.google.com/).

2. **Create a New Project:**
   - Click on the project drop-down and select "New Project."
   - Enter a name for your project and click "Create."

## Step 2: Configure OAuth Consent Screen

1. **Select OAuth Consent Screen:**

   - In the left sidebar, navigate to "APIs & Services" > "OAuth consent screen."

2. **Set User Type:**

   - Choose the appropriate user type for your application (Internal or External).

3. **Configure App Details:**

   - Fill out the required information such as "App name," "User support email," and "Developer contact information."

4. **Save and Continue:**
   - Click "Save and Continue" to proceed.

## Step 3: Create OAuth 2.0 Client ID

1. **Select Credentials:**

   - In the left sidebar, navigate to "APIs & Services" > "Credentials."

2. **Create Credentials:**

   - Click "Create Credentials" and select "OAuth client ID."

3. **Configure OAuth Consent Screen:**

   - Choose "Web application" as the application type.

4. **Authorized Redirect URIs:**

   - In the "Authorized redirect URIs" section, enter the callback URL provided by Aikeedo. This URL is often click-to-copyable for your convenience.

5. **Create Client ID:**

   - Click "Create" to generate the OAuth 2.0 Client ID.

6. **Client ID and Secret:**
   - Note down the generated "Client ID" and "Client Secret" as you'll need them in the next steps.

## Step 4: Configure Aikeedo

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to Google OAuth Settings:**

   - In the admin panel, go to **Settings > Identity providers > Google**.

3. **Enable "Login with Google":**

   - Toggle the switch to enable or disable the "Login with Google" feature.

4. **Enter Google Client ID and Secret:**

   - Input the "Client ID" and "Client Secret" obtained from your Google API project.

5. **Save Changes:**
   - Save your configuration.

## Testing and Usage

Once configured, users will have the option to log in using their Google credentials. They can click "Login with Google," and the OAuth flow will authenticate and authorize them.

By following these steps, you can seamlessly integrate Google OAuth 2.0 into your Aikeedo application.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
