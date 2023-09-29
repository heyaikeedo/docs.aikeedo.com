---
title: SMTP Configuration
nextjs:
  metadata:
    title: SMTP Configuration
    description: Configure your SMTP settings to enable secure and reliable email delivery.
---

Configure your SMTP settings to enable secure and reliable email delivery. {% .lead %}

## Get SMTP Details

Before configuring SMTP settings, you need to obtain the following details from your SMTP server. If you don't have an SMTP server, you can use a third-party service like [SendGrid](https://sendgrid.com/) or [Mailgun](https://www.mailgun.com/).

## Configuration Steps

Follow these steps to set up and validate your SMTP configuration.

1. **Log in as Admin:**

   - Access the Aikeedo admin panel using your administrator credentials.

2. **Navigate to SMTP Settings:**

   - In the admin panel, go to **Settings > Email > SMTP**.

3. **Enter SMTP Details:**

   - Provide the following SMTP details:
     - **SMTP Host:** Enter the address of your SMTP server.
     - **Port:** Specify the port number for your SMTP server.
     - **Username:** Your SMTP server username.
     - **Password:** Your SMTP server password.

4. **Save Changes:**

   - Save your configuration to apply the new SMTP settings.

5. **Validation:**
   - The SMTP configuration will be validated before saving. Ensure that the provided details are correct.

_After successfully saving the SMTP settings, set the mailer transport to SMTP in the [Mail Settings](/email/mail)._

By configuring SMTP settings, you ensure that Aikeedo can securely send emails using your specified SMTP server.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:hey@aikeedo.com).
