## Synopsis

A simple solution for Magento 2 for SMTP mail sending configuration. This code is pre-configured for AWS SES, but it can be adjusted easily for using other providers.

## Motivation

Magento 2 doesn't offer much flexibility when it comes to configuring SMTP settings. There are some extensions out there that cost. And I found some tutorials that aren't too clear. This code is a complete solution and it is accompanied by complete steps to make it work.

## Installation

These instructions are oriented for AWS SES, but as said before - other providers can be used, but you will need to check the settings you need to use.

1. Setup your SES SMTP credentials. For details: http://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-email-smtp.html
2. Update app/code/Kipanga/Email/Model/Transport.php with your SMTP credentials.

Steps to install the extension on Magento 2:
1. Upload app directory to Magento2 root.
2. Using terminal, navigate to the site root directory and run the following commands:
```
php bin/magento module:enable Kipanga_Email
php bin/magento setup:upgrade
php bin/magento setup:di:compile
```

## To do

I know I won't be doing this, as I'm happy with how this works for me. But I'm sure that a keen developer could add the following:
- [ ] Backend UI for managing the settings, rather than doing it directly in the code
- [ ] Predefined templates for common SMTP providers
- [ ] Test email sending and report on errors

Anyway, I hope this helps someone!

I hear your thoughts - what is Kipanga? This is the name of my company for ecommerce solutions, AWS services, etc.

Thanks.