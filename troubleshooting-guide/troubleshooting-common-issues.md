# Troubleshooting Common Issues

This topic would cover the following topics:

1. Is making changes on product not saves ?
2. \[HOW TO]Fix enter your valid Address information Error
3. Change default country in checkout
4. Order products in list layout
5. Options from dropdown cannot be selected
6. Solve jQuery conflict with Multi-categories component
7. Writing template override for the frontend order view and print layouts
8. HOWTO make checkout address field labels language friendly
9. Selling Digital Goods Online with J2Store
10. Joom SEF configuration for J2Store
11. How to Remove + and - Prefix in Product Option Price
12. HOW To Translate the Address Field Labels
13. HOW TO change the colour of add to cart buttons
14. Writing a Layout override for Joomla article manager - An intro image
15. HOWTO solve javascript conflict between some of RocketTheme templates and J2Store
16. How to translate payment option title
17. Hiding Product Options And Cart Button In Category View
18. Override Product Layout
19. HOW TO set up and enable SSL in Joomla
20. How to solve the product link in search results
21. \[HOW TO]Fix product you are trying to access is disabled
22. Is your digital product showing NEVER in expiry column
23. \[HOW TO]Solve terms and conditions popup box freeze

## Is making changes on product not saves ?

Make sure you are not using the MySQL PDO driver of Joomla Go to Global configuration -> Server -> Database settings.

Make sure the Database driver is either MySQL or MySQLi The PDO driver of Joomla has a bug (for a long time).

## \[HOWTO] Change default country in checkout

* Login to Joomla administrator and go to Components -> J2Store Go to Set up> Custom fields
* Open the Country field and choose your default country. Save.
* Open the Zone ID field and choose your default zone. Save.
* Clear Joomla cache and check.

## \[HOWTO] Order products in list layout

The product list layout by default takes the ordering in the Article Manager. However, you can change this ordering (on page load / refresh) via the Menu Parameters.

NOTE: This tutorial applies only for those using the J2Store’s Product List Layout in Version 3. If you use the default article layouts, refer the Joomla documentation on ordering of articles.

Login to Joomla administration and open the menu that links your product list.

Under the Common Options tab, you can find Article Order parameter. There you can choose the ordering method.

![order products](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/troubleshoot\_orderproducts.png)

## \[HOWTO] Options from dropdown cannot be selected

This issue occurs when your site has two instances of the Jquery UI library.

![dropdown](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/options\_dropdown.png)

**In Version 3:**

Go to Configuration - basic settingsSet the Load Jquery UI to Only Front End.Save In Version 2 :Go to J2Store - Options - Basic settingsSet the Load Jquery UI to Only Front End.Save.

## \[HOWTO] solve jQuery conflict with Multi-categories component

If you are using the Multi-cateogies component (which adds the ability to choose more than one category for your articles), you might experience a jQuery conflict with J2Store. Here is a quick fix

Are you using Multi-categories component ?If yes, then the issue comes due to loading of multiple Jquery UI instances.

Here is a quick fix

Open /administrator/components/com\_j2store/helpers/strapper.php

Around line 33, you will find $document->addScript(JURI::root(true).’/media/j2store/js/j2storejqui.js’);

Change this to if($mainframe->isSite()) {$document->addScript(JURI::root(true).’/media/j2store/js/j2storejqui.js’);}

Save.

Logout. Clear browser cache and test.

This should fix the issue.
