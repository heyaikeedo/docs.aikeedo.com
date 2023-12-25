---
title: How to install in cPanel (Add-on Domain or Subdomain)
nextjs:
  metadata:
    title: How to install in cPanel (Add-on Domain or Subdomain)
    description: Follow these step-by-step instructions to install Aikeedo in cPanel.
---

Follow these step-by-step instructions to install Aikeedo in cPanel. {% .lead %}

## Prerequisites

Before you begin, ensure that you have configured your server. For more information, refer to the [Server Requirements](/get-started/requirements) guide.

## Installation Steps

For this guide, we will assume that:

- the username for your cPanel account is `username`
- your add-on (or subdomain) domain is `yourdomain.com`
- the root directory for your add-on (or subdomain) domain is `/home/username/yourdomain.com`

It's important to note that, all pathes here are absolute pathes, `/home/username` part might be hidden in various pages of cPanel such file manager etc. In this case, instead of `/home/username/yourdomain.com`, you might see `/yourdomain.com`.

1. **Upload Archive:**

   - Locate the archive named **aikeedo-server-files.zip** in the extracted package.
   - If you couldn't find the file, refer to the [File Structure](/get-started/file-structure) guide for assistance.
   - Upload the **aikeedo-server-files.zip** archive to `/home/username/yourdomain.com`

2. **Extract Files on the Server:**

   - Extract **aikeedo-server-files.zip** archive on the server to the same directory where you uploaded the archive in the previous step.

3. **Configure domain root public directory:**

   - Find the **public** directory inside the extracted archive. This directory contains all the files that should be accessible to the public. This directory should be located at `/home/username/yourdomain.com/public`

4. **Update domain root directory:**

   - In cPanel, go to **Domains** > **Addon Domains** (or **Subdomains**).
   - Click on **Manage** next to your add-on (or subdomain) domain.
   - Update the **Document Root** to `/home/username/yourdomain.com/public` and click on **Change**.

5. **Access Installation Page:**

   - Open a web browser and enter your domain or subdomain URL.
   - It should automatically redirect you to the installation page located at `/install`.

6. **Follow On-Screen Instructions:**

   - The installation wizard will guide you through the setup process.
   - You will be prompted to provide Database Credentials, Purchase Code, and Admin Account Details.
   - Follow the instructions carefully to complete the installation.

7. **Complete Installation:**
   - Once you have provided all the necessary information, the installation wizard will finalize the setup.
   - Confirm that the installation was successful, and you're ready to explore Aikeedo.

Congratulations! You've successfully installed Aikeedo.

Thank you for choosing Aikeedo. Enjoy the power of AI in your content creation endeavors!

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
