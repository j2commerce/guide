# Migrating from 2.x to3.x

## Introduction <a href="#introduction" id="introduction"></a>

Version 3 is re-written from scratch using the FOF Framework for Joomla. It comes with loads of new features and follows a different table structure (schema). So a migration is required if you want to update your store from 2.x to Version 3.

We have created a tool, which simplifies the migration of your 2.x store to the latest 3.x version.

```
Please read the documentation carefully before you attempt the migration.
```

## Actions to be taken before migration <a href="#actions-to-be-taken-before-migration" id="actions-to-be-taken-before-migration"></a>

Please install Akeeba Backup, which is one of the best backup apps available for Joomla (and it is free! ) and take a **FULL BACKUP** of your site.

```
**Warning**
If you proceed without taking a BACKUP and if you want to revert back to the old version, you will end up going in the toughest route. So please take a FULL BACKUP of your site before proceeding with the migration
```

Also

* Make sure your J2Commerce version is 2.8.x or later
* If you are using an old 2.x version, first update it to 2.8.x
* Set your site offline
* Set Error Reporting to None in the Global Configuration

## Pre-requisites <a href="#pre-requisites" id="pre-requisites"></a>

1. Joomla 3.3.x
2. J2Commerce 2.8.0 or later

You can use the migration tool only when your Joomla version is 3.3 or later. If you are currently running the store in Joomla 2.5, please consider upgrading your website to latest Joomla version because the Joomla 2.5 life has ended in December 2014 itself.

## Download Migration Tool <a href="#download-migration-tool" id="download-migration-tool"></a>

You can download the migration tool directly from the following url: [click here](https://bitbucket.org/j2store/j2store_migration/downloads).

## Using the Migration Tool <a href="#using-the-migration-tool" id="using-the-migration-tool"></a>

### 1. Installation <a href="#id-1-installation" id="id-1-installation"></a>

You can use the standard Joomla installer for installing the tool.

Login to Joomla administrator and go to Extension Manager and install the tool

### 2. Backup! Backup! Backup! <a href="#id-2-backup-backup-backup" id="id-2-backup-backup-backup"></a>

Take a FULL BACKUP of your website using Akeeba Backup. If you proceed without taking a BACKUP, you will not be able to recover your data in case something went wrong.

The Tool will not allow you to proceed if you do not have the Akeeba Backup component installed. We had to force this check because some Joomla web masters do not have the habit of taking regular backup of their site.

### 3. Important points to note down <a href="#id-3-important-points-to-note-down" id="id-3-important-points-to-note-down"></a>

J2Commerce Version 3 is completely re-written from scratch. We have made quite a lot of structural changes. So some of the product types require additional inputs after the migration.

**3.1 Variant stock**

If you are to maintain stock for product options (aka Variable product), the tool will migrate all the data except SKU, Price and Stock.

These products will be treated as Variable Product types. The tool will list the products that fall under the variable product type. Please note down the Article IDs.

Once the migration process is completed, go to Article manager and open these articles. Click Generate variants button (J2Commerce cart -> Variants tab). Once generated, click Edit against each variant and then enter the SKU, Price and Stock.

**3.2 Downloadable products**

The tool will migrate all the data of your downloadable products. There are few changes in the structure of the downloadable products in J2Commerce Version 3.

**3.2.1 Download Limit**

Earlier, download limit was set against each file. But now, the limit is set per product. Plus, there is an expiry control. You can set the download availability to expire XX days after the order is confirmed.

The limit and the expiry control has to be set by opening all your products. Otherwise, J2Commerce v3 will not limit the number of downloads per user.

### 4. Prepare for migration <a href="#id-4-prepare-for-migration" id="id-4-prepare-for-migration"></a>

Once all checks passed, the tool will display the Prepare for Migration button. Click the button. It will backup all your J2Commerce 2.x tables Once backup is done, you can see the Start Migration button

### 5. Start Migration <a href="#id-5-start-migration" id="id-5-start-migration"></a>

Click the Start Migration button and wait. The tool will migrate the data, remove old modules, install the new tables / db schema for J2Commerce version and uninstall old J2Commerce version 2.x.

If the migration is successful, you can will see a success message. If there is an error, it will display the error.

**5.1 What should I do if an error has occured?**

Please post the error at the forum: [click here](http://j2store.org/forum/j2store-version-3-feedback.html)

### 6. Install Version 3 <a href="#id-6-install-version-3" id="id-6-install-version-3"></a>

Download J2Commerce Version 3 latest version from the site and install it. Free users can download from [click here](http://j2store.org/download.html)

PRO users can download the PRO version from [click here](http://j2store.org/my-downloads.html)

### 7. Post Migration <a href="#id-7-post-migration" id="id-7-post-migration"></a>

Once migration is successful, download the latest J2Commerce Version 3 from our site and install it.

Then Go to Joomla administrator -> Components -> J2Commerce

* Go to Set up - Configurations
* Review the parameters and set them up as per your requirements.
* Go to Catalog - Products - Open a product
* Check if everything is right and save it.

**No check on email-adress with guest checkout.Why?**

Once finished the migration, Please go to J2Commerce - Configuration -Checkout layout. Click Re-populate checkout layout. Save. While migrating, the email field was set to not validate on guest checkout. Re-setting the checkout layout and also setting the email field to YES in the J2Commerce - Set up custom fields solves the issue.

## Reverting back to 2.x after the migration <a href="#reverting-back-to-2x-after-the-migration" id="reverting-back-to-2x-after-the-migration"></a>

```
VERY IMPORTANT: Apply the following steps only if you migrated from 2.8.x to 3.x and then want to downgrade. You should be familiar with Joomla tables and PhpMyAdmin operations. Otherwise, **NEVER EVER** attempt this if you DO NOT understand any of the steps below.
```

**Step 1:** Backup your site using Akeeba Backup

\*\*Step 2: \*\* Uninstall J2Commerce version 3

**Step 3:** Go to Phpmyadmin

You will see

a. Tables with the follwing prefix:

\_v2\_j2commerce\_ = These are your 2.x tables backed up by the migration tool

b. Tables with the prefix: j2commerce = these are j2commerce 3.x tables

Delete the tables with the prefix j2commerce

Rename the \_v2\_j2commerce\_ tables to j2commerce

Example: \_v2\_j2commerce\_orders to \_j2commerce\_orders

**Step 4:** Install J2Commerce 2.8.x version.
