---
title: Billing Configuration
nextjs:
  metadata:
    title: Billing Configuration
    description: Customize your billing settings in Aikeedo to align with your business model and user onboarding strategy.
---

Customize your billing settings in Aikeedo to align with your business model and user onboarding strategy. {% .lead %}

## Set Default Currency

Choose the default currency for your billing system. Ensure that your selected payment gateway supports the chosen currency to avoid any issues during transactions.

## Define Trial Period Days

Set the trial period duration for new users. A value of 0 disables the trial period. Keep in mind that each user is eligible for a trial only once in any paid plan.

## Sign Up Plan

Select the plan to which new users will be automatically subscribed without providing payment details. This feature streamlines the onboarding process. Choose "None" to disable automatic subscription, requiring users to choose a plan themselves.

{% callout type="warning" %}
If selecting any paid plan for automatic subscription, it's highly recommended to enable the trial period. Otherwise, new users will be able to access the selected paid plan for free.
{% /callout %}

## Fallback Plan

Define the plan that users will be automatically subscribed to if any subscription expires or fails to renew. This acts as a fallback mechanism. Choose "None" to disable automatic downgrading, requiring users to choose a new plan themselves.

{% callout type="note" %}
Ensure that you have created appropriate pricing plans before selecting the Sign-Up and Fallback plans to ensure a smooth user experience.
{% /callout %}

By configuring these billing settings, you can tailor the subscription process to meet the needs of your business and users. I

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:hey@aikeedo.com).
