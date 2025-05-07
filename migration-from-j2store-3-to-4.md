---
description: The guide helps you migrate your J2Commerce 3 to J2Commerce 4
---

# Migration from J2Commerce 3 to 4

This article is a guide for those looking to migrate from J2Commerce 3 to J2Commerce 4 so that they can upgrade their Joomla version to the latest Joomla 4.

{% hint style="warning" %}
<mark style="color:red;">**The following instructions apply ONLY IF you have a Joomla 3 website with J2Commerce 3.**</mark>
{% endhint %}

{% hint style="warning" %}
<mark style="color:orange;">**IMPORTANT: Please carefully read the instructions and try the migration in a staging / development / testing copy of your site. There are a number of breaking changes. If you attempt to migrate directly in a live environment, it may lead to site crashing / fatal errors.**</mark>

<mark style="color:orange;">**So attempt the migration in a testing / staging copy of your site first.**</mark>
{% endhint %}

{% hint style="danger" %}
**CAUTION:**

While we are committed to ensuring a smooth transition, please note that unforeseen circumstances may arise during the migration process. Example: You might have an incompatible plugin, a third-party extension that conflicts with J2Commerce and so on.

Though we'll make every effort to assist, we cannot be held accountable for potential issues that may occur as a result. Proceed with caution.
{% endhint %}

### Step 1: BACKUP, BACKUP, BACKUP

Please take a FULL BACKUP of your site before you start the migration process. Since there are a number of breaking changes in J2Commerce 4, there are chances of fatal errors.

Take a FULL BACKUP so that in case of issues, you can always restore your site from the backup.

### Step 2: Install the migration helper utility

We have created a simple migration helper that check for potential conflicts with the plugins and lets you disable them before the migration.

1. Download the utility from here: [github.com/j2commerce/j2store\_migration\_checker/releases](https://github.com/j2commerce/j2store_migration_checker/releases)
2. Install it by logging into your Joomla 3 administrator -> extensions -> Install
3. Once installed, go to Components -> J2Migration checker

### Step 3: Disable the Plugins / modules and apps of J2Commerce

The migration helper will list all the J2Commerce plugins, apps, modules, extensions that needs to be disabled before you can proceed with it.

Once you have disabled them, you will see a “green light” for proceeding with the migration.

{% hint style="warning" %}
IMPORTANT: Please take note of the list of plugins you have there as they need to be upgraded individually with their respective Joomla 4 compatible versions.

We will be publishing the Joomla 4 compatibility for the official J2Commerce plugins / apps / modules / extensions one by one. You can check our Extensions page for a list of available extensions for J2Commerce with Joomla 4 compatibility.
{% endhint %}

If you have any custom developed extension for J2Commerce, please reach out to the respective vendors / developers for compatibility.

We’ll not be able to support any custom developed extensions / plugins / add-ons / modules.

### Step 4: Install J2Commerce 4

Once you have disabled all the J2Commerce related extensions, you can proceed to download the J2Commerce 4 from our official J2Commerce Github repository at:

[github.com/j2commerce/j2cart/releases](https://github.com/j2commerce/j2cart/releases)

Download the latest version of J2Commerce 4 and install it.

### Step 5: Upgrading J2Commerce plugins

Please check our extensions section to get the latest version of the J2Commerce plugins / apps / modules / extensions you have in your site.

You need to install the Joomla 4 compatible version of all the J2Commerce plugins / apps / modules / extensions you have in your site before you can upgrade to Joomla 4.

We will be publishing the Joomla 4 compatible J2Commerce plugins / extensions soon.

### Step 6: Ensure all the plugins / extensions in your site are Joomla 4 compatible.

\
If you have other extensions / plugins / modules from third party developers, you need to check their Joomla 4 compatibility before upgrading to Joomla 4.

Just upgrading J2Commerce 3 to J2Commerce 4 will not ensure compatibility for Joomla 4. All the extensions and plugins that you use in your site should be Joomla 4 compatible before you upgrade.

{% hint style="danger" %}
Upgrade to Joomla 4 only after ensuring all the plugins / extensions in your site are Joomla 4 compatible.
{% endhint %}
