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

## Writing template override for the frontend order view and print layouts

This tutorial applies to J2store 3.x versions. You will nedd to use your hosting CPanel file manager or an FTP client like filezilla to carry out the following tasks.

The following file control the display of order details in frontend. orderitems.php = This controls the display the order details in email and invoice template(frontend order view)

Let us see how to override the orderitems.php

Copy /components/com\_j2store/views/myprofile/tmpl/orderitems.php

to  /templates/YOUR_TEMPLATE/html/com\__j2store/myprofile/orderitems.php

Edit the file /templates/YOUR_TEMPLATE/html/com\__j2store/myprofile/orderitems.php

Make your changes on overrides. Save. You need to do the same if you want to override.

## HOW TO make checkout address field labels language friendly

In a multi-lingual Joomla site, the checkout step doesn’t convert to other language and seems to still show in english. How to make it appear in your own language ?Simple, just rename the custom field labels as follows and it will quickly consider picking the language strings from your local language pack.

Still if you do not see the translation, please check your language pack for the following strings and translate them in your language.

language file location /administrator/language/en-GB/en-GB.com\_j2store.ini

**J2STORE\_ADDRESS\_TYPE="Address type" J2STORE\_BILLING\_ADDRESS="Billing Address" J2STORE\_SHIPPING\_ADDRESS="Shipping Address" J2STORE\_ADDRESS\_DETAILS="Address Details" J2STORE\_ADDRESS\_FIRSTNAME="First name" J2STORE\_FIRST\_NAME="First Name" J2STORE\_ADDRESS\_LASTNAME="Last name" J2STORE\_LAST\_NAME="Last Name" J2STORE\_ADDRESS\_USER\_ID="User ID" J2STORE\_ADDRESS\_USERNAME="Username" J2STORE\_ADDRESS\_LINE1="Address Line 1" J2STORE\_ADDRESS1="Address Line 1" J2STORE\_ADDRESS\_LINE2="Address Line 2" J2STORE\_ADDRESS2="Address Line 2" J2STORE\_ADDRESS\_CITY="City"**&#x20;

**J2STORE\_CITY="City"**&#x20;

**J2STORE\_ADDRESS\_ZIP="Zip / Postal code" J2STORE\_ADDRESS\_STATE="State" J2STORE\_ADDRESS\_COUNTRY="Country" J2STORE\_ADDRESS\_PHONE="Phone" J2STORE\_ADDRESS\_MOBILE="Mobile"**&#x20;

**J2STORE\_ADDRESS\_FAX="Fax" J2STORE\_ADDRESS\_COMPANY\_NAME="Company" J2STORE\_ADDRESS\_TAX\_NUMBER="Tax Number" J2STORE\_ADDRESS\_ZONE="Zone / Region" J2STORE\_TELEPHONE="Telephone" J2STORE\_ADDRESS\_EDIT="View/Edit Address" J2STORE\_SHOPPER\_ADDRESSES="Shopper Addresses"**

## Selling Digital Goods Online with J2Store

Selling ebooks, PDF, images and files online is easy with the J2Store Joomla shopping cart. Here is a step-by-step guide to set up your digital downloads.

**Step 1: Let us create a folder on your site to upload the files**

You can use your Hosting Providers CPanel File manager or an FTP client like FileZilla to access your web root (public\_html / www / httpdocs ) Once you are in the web root, create a folder. Let us name it as: myfiles

**Step 2: Protect the folder from outside access**

We do not want people to access this folder using their browser and download files. So let us protect this folder using a .htaccess file.

* Create a file called htaccess.txt in your computer and open it with your favorite text editorAdd the following lines to it
* order deny, allow or deny form all
* Save the file. Now upload it to the folder we just have created in our web root. In our example, it is myfiles

> IMPORTANT: Rename it as .htaccess

All the files uploaded to this folder is now protected.

**Step 3: Point J2Store to use the files in this folder.**

1. Go to Joomla adminj2storeConfigurationBasic settings.
2. In Folder path for digital goods, enter the name of the folder that contains your files. In our example, it is: myfiles
3. Save the configuration.

**Step 4: Creating your first digital product**

1. J2Store uses Joomla articles as products. So head to Joomla admin -> Article Manager and create an article.
2. Fill in the title, description, add an image and set all other fields and Save.
3. Go to J2Store cart tab and set all the fields and Save.
4. Now go to files tab in the navigation you can see Set product files button.

![product down files](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/product\_down\_files\_1.png)

![product down files2](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/product\_down\_files\_2.png)

## Solving the missing currency symbol in your store

When you install, J2Store sets USD as the default currency. When store owners change the currency code, they often forgot to update their default currency in their store profile.

When you see the currency symbol missing, it is an indication that:

1. You have either changed the currency code or deleted the USD and then created a new currency for your country.
2. You forgot to reflect these changes in the Store profile.

SolutionGo to J2Store admin -> Set up - > -> configuration -> Store

Choose your Default Currency.

**IMPORTANT:**Hit the Save button. Even if you see your currency is selected by default, it may not be saved in the store profile database. Since it is the only currency available (you deleted the USD or any other currency), the dropdown list shows the first currency available.

So CLICK the SAVE button. Still not seeing the Currency symbol, open your store again and click SAVE again.

## Joom SEF configuration for J2Store

If you are using JoomSEF along with J2Store, you will need to make simple change in the configuration. Go to JoomSEF configuration -> Advanced Configuration. Change the Set Page base href value to Yes - always use only base URL.

## How to Remove + and - Prefix in Product Option Price

Store owners sometimes want to hide the + (PLUS) and the - (MINUS) prefix that is shown along with the product options. In J2Store Version 3, you turn off the price prefix with a switch.

**Default Joomla article layouts (like Category blog layout):**

1. Go to J2StoreConfigurationProduct tab.
2. Set Product option price prefix to HIDE
3. Save

![priceprefix1](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/priceprefix\_1.png)

**Product list layout:**

If you use the J2Store’s product list layout, then you will find a similar switch in the menu parameters.

* Open the menu that links your product list layout and go to Common Options.
* Set Product option price prefix to HIDE
* Save

![priceprefix2](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/priceprefix\_2.png)

## HOW To Translate the Address Field Labels

If you wanted to translate the Address field labels, you can enter your translation in the respective fields.Go to Joomla admin -> J2Store -> Set up -> Custom Fields

Open the field, the label of which you want to change, and enter your translation in the label field.

**Multi-lingual sites**

if you are running multi-lingual site, you can enter a language constant in the label field.Example: J2STORE_MY_FIELD\_NAME

* Then you can go to Language manager and create an Override. IMPORTANT: Set the Filter to Administrator before you create an override.
* Click New
* Language Constant: J2STORE_MY_FIELD\_NAME
* Text: Your translation
* Check the For Both locations
* Save.

![language override](https://raw.githubusercontent.com/j2store/doc-images/master/troubleshooting-guide/troubleshooting-common-issues/translation\_addres\_fields.png)

You can repeat this steps for your second, third, and other languages.

You can use language strings in all the fields including Custom Error message, Option Titles (if field type is select, radio, checkbox).

## HOW TO change the colour of add to cart buttons

A majority of those who wanted to change the colour of the buttons are using template with a template that does not support the Twitter bootstrap framework, which helps you make your site responsive.

We have added a name-spaced bootstrap css in the J2Store package. So if your template does not support bootstrap, J2Store will use the bootstrap CSS included in the package. If your template supports bootstrap, then J2Store will inherit your template style, without you changing any CSS.

The following is a guide to those who want to change the button colours

Open your template’s css file located in /templates/YOUR\_TEMPLATE/css folder.

At the end of the file, add the following CSS. Save the file. Clean your browser cache and joomla cache. Refresh.

**Add to cart button**

.j2store .btn-primary {background: #FF0000 !important; /\*this will change your button colour to red. You can change the hex colour code based on your choice \*/

```
color: #FFFFFF !important; /*this will change your text on the button to white. You can change the hex colour code based on your choice */

}

**View cart button**

.j2store .btn-success {

background: #FF0000 !important;

color: #FFFFFF !important;

}

.j2store .btn-success:hover {

background: #FF0000 !important;

color: #FFFFFF !important;

}

**Update button**

.j2store .btn-warning {

background: #FF0000 !important;

color: #FFFFFF !important;

}

.j2store .btn-warning:hover {

background: #FF0000 !important;

color: #FFFFFF !important;

}
```

## Writing a Layout override for Joomla article manager - An intro image

Layout overrides is a feature introduced in Joomla 3. They provide more modularity for templates across views and avoid duplication of code for a same design. Consider a situation In Joomla caregory blog layout, you have to make a Joomla Article intro image a hyperlink with the read more button link. If you are using prostar template you can use this below.

**Step 1: Write a layout override**

You can use a file manager in your Hosting Control panel or an FTP client like FileZilla for doing the following tasks.

Copy

JOOMLA-ROOT/layouts/joomla/content/intro\_image.php

to

JOOMLA-ROOT/templates/TEMPLATE>/html/layouts/joomla/content/introimage.php

**Step 2: Edit the override layout**

Find below code

```
$params = $displayData->params; ?> images); ?> image_intro) && !empty($images->image_intro)) : ?> float_intro)) ? $params->get('float_intro') : $images->float_intro; ?>image_intro_caption): echo 'class="caption"' . ' title="' . htmlspecialchars($images->image_intro_caption) . '"'; endif; ?> src="/image_intro); ?>" alt="image_intro_alt); ?>" itemprop="thumbnailUrl"/> 

```

Replace above code with following code\


```
$params  = $displayData->params;
if ($params->get('access-view')) :
$link = JRoute::_(ContentHelperRoute::getArticleRoute($displayData->slug, $displayData->catid));
else :
$menu = JFactory::getApplication()->getMenu();
$active = $menu->getActive();
$itemId = $active->id;
$link1 = JRoute::_('index.php?option=com_users&view=login&Itemid=' . $itemId);
$returnURL = JRoute::_(ContentHelperRoute::getArticleRoute($displayData->item->slug, $displayData->item->catid));
$link = new JUri($link1);
$link->setVar('return', base64_encode($returnURL));
endif;
?>
images); ?>
image_intro) && !empty($images->image_intro)) : ?>
float_intro)) ? $params->get('float_intro') : $images->float_intro; ?>

```

Once you have finished editing, save the changes. Now you are done.\


**NOTE:** If something went wrong, just delete.\


JOOMLA-ROOT/templates/TEMPLATE>/html/layouts/joomla/content/introimage.php\
and go to Step 1.\

