---
description: J2Commerce (formerly known as J2Store)
---

# Pagseguro Payment plugin

This plugin integrates Pagseguro payment gateway with J2store. PagSeguro is an e-commerce tool that mediates payments for both sellers and buyers. It offers different paying methods to the buyers.

## System Requirements <a href="#system-requirements" id="system-requirements"></a>

* PHP 8.1.0 +
* Joomla! 4.x/ Joomla! 5.x +
* J2Commerce / J2Store 4.x +

## Installation Instructions <a href="#installation-instructions" id="installation-instructions"></a>

1. Use the Joomla installer to install the plugin.
2. In the backend, go to J2store Dashboard -> Payment methods and enable plugin.
3. Open the plugin and enter the parameters (read the explanation about each parameter given below)
4. Save and close it.

## Configuration <a href="#configuration" id="configuration"></a>

The plugin has the following parameters need to be addressed.

**Payment option title** The value entered here will be used as the title for this payment method. Customer will see this value when he checks out.

**Plugin Display Image** This image will be displayed while payment options are listed in the checkout page.

**Email** Enter the Email address which you have given during your signup.

**Pagseguro Token** Enter the pageseguro token provided by the pagseguro payment.

**Use Sandbox** Pagseguro offers a testing suite called Sandbox. Before going live, you can test your store using the pagseguro’s sandbox feature.

![pagseguro](https://raw.githubusercontent.com/j2store/doc-images/master/payment-methods/pagseguro-payment-plugin/pagseguro_1.png)

**Sandbox Email** Enter your pagseguro’s sandbox Email ID.

**Sandbox Pagseguro Token** Use your pagseguro’s sandbox token.

**Article Id for Thank you message** You can create a Joomla Article to say thanks to the users, who purchased in your online store. Enter the article ID here.

**Geozone** By selecting a geozone here, you can restrict this payment method to only customers of that geo-region. Choose All geozones to show this method to all customers.

**Display text on selection** The text entered here will be displayed when customer selects this payment method. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. For example, enter a language constant:

J2STORE\_TEXT\_TO\_DISPLAY\_ON\_SELECTION.

Now you can go to Joomla admin-> Language Manager->Overrides and create overrides for the language constant in all your languages.

**Display text before payment** The text entered here will be displayed to the customer at the order summary screen before he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

![psgplugin](https://raw.githubusercontent.com/j2store/doc-images/master/payment-methods/pagseguro-payment-plugin/pagseguro_2.png)

**Display text on after payment** The text entered here will be displayed when customer completes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display text on error in payment** The text entered here will be displayed to the customer when there is an error in the payment process. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display text if customers cancels payment** The text entered here will be displayed to the customer when he cancels the payment at the gateway (NOT in your site). You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Payment button text** Text entered here will be added as the name of the payment button. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override.

**Debug** Choose YES to enable the debug mode. If you set this to yes, then debug messages will be logged and saved in the cache folder in your Joomla root directory. DO NOT select YES in the live site.

![psgpayment](https://raw.githubusercontent.com/j2store/doc-images/master/payment-methods/pagseguro-payment-plugin/pagseguro_3.png)

**Support**

Still have questions? You can post in our support forum: [click here](http://j2store.org/forum/index.html)

Thank you for using our extension.
