---
title: Server Requirements
nextjs:
  metadata:
    title: Server Requirements
    description: Aikeedo is a web-based application that requires a server environment to run. Ensure a smooth installation and operation of Aikeedo by meeting the following server requirements.
---

Aikeedo is a web-based application that requires a server environment to run. Ensure a smooth installation and operation of Aikeedo by meeting the following server requirements. {% .lead %}

## PHP and MySQL Versions

- **PHP:** 8.2 or later
- **MySQL:** 8.0 or later

## Required PHP Extensions

Make sure the following PHP extensions are installed:

- `ctype`
- `curl`
- `dom`
- `fileinfo`
- `intl`
- `json`
- `libxml`
- `mbstring`
- `openssl`
- `pcre`
- `phar`
- `simplexml`
- `tokenizer`
- `xml`
- `xmlwriter`
- `zip`

_Note: Some additional extensions might be required, but these are generally installed by default._

## php.ini Configuration

Ensure the following configurations in your `php.ini` file:

- **File Uploads:** On
- **Post Max Size:** 25MB or more
- **Upload Max Filesize:** 25MB or more

## Webserver Compatibility

Aikeedo is tested and compatible with the following webservers:

- **Apache**
- **Nginx**

However, it is designed to work seamlessly with any webserver, providing you with flexibility in choosing the server that best fits your needs.

Meeting these server requirements ensures that Aikeedo operates at its full potential, delivering a robust and efficient AI-powered content creation experience.

Links:

- How to configure php.ini? [Click here](https://www.php.net/manual/en/configuration.file.php)
- How to create MySQL database? [Click here](https://dev.mysql.com/doc/mysql-getting-started/en/)
- How to install Apache? [Click here](https://httpd.apache.org/docs/2.4/install.html)
- How to install Nginx? [Click here](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/)

Thank you for choosing Aikeedo! Get ready to experience the future of AI-powered content creation!

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
