---
title: How to install in cPanel (Main Domain)
nextjs:
  metadata:
    title: How to install in cPanel (Main Domain)
    description: Follow these step-by-step instructions to install Aikeedo in cPanel.
---

Follow these step-by-step instructions to install Aikeedo in cPanel. {% .lead %}

## Prerequisites

Before you begin, ensure that you have configured your server. For more information, refer to the [Server Requirements](/get-started/requirements) guide.

## Installation Steps

For this guide, we will assume that the username for your cPanel account is `username`.

It's important to note that, all pathes here are absolute pathes, `/home/username` part might be hidden in various pages of cPanel such file manager etc. In this case, instead of `/home/username/public_html`, you might see `/public_html`.

1. **Upload Archive:**

   - Locate the archive named **aikeedo-server-files.zip** in the extracted package.
   - If you couldn't find the file, refer to the [File Structure](/get-started/file-structure) guide for assistance.
   - Upload the **aikeedo-server-files.zip** archive to one level upper directory of cPanel's **public_html** directory. For example, if the full path of the **public_html** directory is `/home/username/public_html`, then upload the archive to `/home/username/`. This is generally the root directory in cPanel file manager.

2. **Extract Files on the Server:**

   - Extract **aikeedo-server-files.zip** archive on the server to the same directory where you uploaded the archive in the previous step.

3. **Configure domain root public directory:**

   - Find the **public** directory inside the extracted archive. This directory contains all the files that should be accessible to the public. Do not confuse the **public** directory with default cPanel's **public_html** directory. If you've followed the previous steps correctly, the full path of the **public** directory should be `/home/username/public`.
   - Copy all files from the `/home/username/public` directory into the `/home/username/public_html` directory.
   - **Important:** Ensure to copy the `/home/username/public/.htaccess` file, which might be hidden in cPanel's file manager.
   - In the `/home/username/bootstrap/container.php` file, update line 21 as below:

   ```php
   $webroot = $rootDir . '/public_html';
   ```

4. **Access Installation Page:**

   - Open a web browser and enter your domain URL.
   - It should automatically redirect you to the installation page located at `/install`.

5. **Follow On-Screen Instructions:**

   - The installation wizard will guide you through the setup process.
   - You will be prompted to provide Database Credentials, Purchase Code, and Admin Account Details.
   - Follow the instructions carefully to complete the installation.

6. **Complete Installation:**
   - Once you have provided all the necessary information, the installation wizard will finalize the setup.
   - Confirm that the installation was successful, and you're ready to explore Aikeedo.

Congratulations! You've successfully installed Aikeedo.

Thank you for choosing Aikeedo. Enjoy the power of AI in your content creation endeavors!

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
