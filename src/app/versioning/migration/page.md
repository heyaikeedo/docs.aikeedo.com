---
title: Migration
nextjs:
  metadata:
    title: Migration
    description: Learn how to migrate your current installation of Aikeedo to the latest version and benefit from the latest features and improvements.
---

Learn how to migrate your current installation of Aikeedo to the latest version and benefit from the latest features and improvements. {% .lead %}

**Instructions to migrate to v2.0**

1. **Take a backup:**

   - Before migrating your current installation of the Aikeedo v1.x its highly recommended to take a full backup of database and files

2. **Update files:**

   - As described in the [installation guide](/get-started/installation), upload server files to your server and extract the zip archive to the current installation directory. Owerrite all files.

3. **Set installation environment::**

   - Locate the `.env` file in the root directory of the Aikeedo installation and copy the database credentials to a safe place.

   - Update the ENVIRONMENT value in `.env` file to `install`

     ```env
     ENVIRONMENT=install
     ```

     Alternatively, you can remove the `.env` file from the root directory of the app.

4. **Access Installation Page:**

   - Open a web browser and enter your domain or subdomain URL.
   - It should automatically redirect you to the installation page located at `/install`.

5. **Follow On-Screen Instructions:**

   - The installation wizard will guide you through the setup process.
   - You will be prompted to provide Database Credentials, Purchase Code, and Admin Account Details.
   - You you're prompted for Database Credentials, use the same credentials as in the `.env` file.
   - Follow the instructions carefully to complete the installation.

6. **Complete Installation:**
   - Once you have provided all the necessary information, the installation wizard will finalize the setup.
   - Confirm that the installation was successful, and you're ready to explore Aikeedo.

Keeping Aikeedo updated ensures that you benefit from the latest advancements, security patches, and performance enhancements.

Thank you for choosing Aikeedo! Get ready to experience the future of AI-powered content creation!

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
