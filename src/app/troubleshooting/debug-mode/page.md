---
title: Debug Mode
nextjs:
  metadata:
    title: Debug Mode
    description: Debug mode is a feature in Aikeedo that provides detailed information about errors and issues, making it easier for developers to identify and fix problems during development. By default, Aikeedo has debug mode enabled during the installation process, which provides detailed error information for development and debugging purposes. After a successful installation, debug mode is automatically disabled to enhance security and reduce the risk of exposing sensitive information.
---

Debug mode is a feature in Aikeedo that provides detailed information about errors and issues, making it easier for developers to identify and fix problems during development. By default, Aikeedo has debug mode enabled during the installation process, which provides detailed error information for development and debugging purposes. After a successful installation, debug mode is automatically disabled to enhance security and reduce the risk of exposing sensitive information. {% .lead %}

## `.env` file configuration

Debug mode can be managed by adjusting the `DEBUG` setting in the `.env` file located in the application's root directory. The `.env` file is a configuration file that holds various settings for the Aikeedo application.

### Enabling Debug Mode

To enable debug mode, set the `DEBUG` variable to `1`:

```ini
DEBUG=1
```

### Disabling Debug Mode

To disable debug mode, set the `DEBUG` variable to `f0`:

```ini
DEBUG=0
```

## Recommendations

It is highly recommended to keep debug mode disabled in a production environment. Enabling debug mode in production poses security risks and may expose sensitive information. In a development environment, you might find debug mode helpful for identifying and fixing issues during the development and testing phases.

By understanding how to adjust the `DEBUG` setting in the `.env` file, you can easily control the debug mode status in Aikeedo. Remember to exercise caution and follow security best practices, especially in production environments.

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
