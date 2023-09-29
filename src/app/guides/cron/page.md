---
title: Subscription Renewal Configuration
nextjs:
  metadata:
    title: Subscription Renewal Configuration
    description: Ensure smooth and timely renewal of subscription usages in Aikeedo by configuring a proper cron task.
---

Ensure smooth and timely renewal of subscription usage credits in Aikeedo by configuring a proper cron task. Follow these guidelines to set up the cron task for subscription renewal: {% .lead %}

## Frequency and Interval

- **Frequency:** Subscription usages are intended to be renewed every 30 days.
- **Interval:** The cron task should ideally run once per minute for timely renewals.

{% callout type="note" %}
In some servers, the minimum interval for running cron tasks is 15 minutes. If this is the case, subscriptions will still be renewed, but there might be a delay of up to approximately 15 minutes.
{% /callout %}

## Cron Task Configuration

Set up the cron task by creating an entry similar to the following in your server's crontab:

```shell
* * * * * /usr/bin/php /path/to/app/root/cron.php
```

This cron task runs the specified PHP script (`cron.php`) using the PHP binary (`/usr/bin/php`). Ensure to replace `/path/to/app/root/` with the actual path to your Aikeedo application's root directory.

## Troubleshooting

If you encounter issues with subscription renewals, consider the following:

- Verify the correctness of the cron task configuration.
- Check server logs for any error messages related to the renewal process.

By setting up and monitoring the cron task, you ensure that subscription usages are renewed in a timely manner, providing a seamless experience for your users. If you have any questions or need further assistance, refer to our documentation or contact our support team. Thank you for choosing Aikeedo!

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
