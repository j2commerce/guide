---
description: J2Commerce (formerly known as J2Store)
---

# Paypal Pro Payment Plugin

This plugin integrates with Paypal Pro Payments using the Direct API.

**Installation** You can use the standard Joomla installer for installing the plugin. Go to Extensions and choose the plugin package to install.

**Configuration** Go to Joomla Administraton->Extensions->Plugin Manager Open the Paypal Pro plugin.

TIP: Set the type filter to J2Store to quickly get to the plugin

**Payment Option Title** Enter a title for this payment option. Customers can see this title while selecting the payment.

**Plugin Display Image** Image to be shown while PayPal PRO option in listed in checkout page.

**API User Name** The API username provided by Paypal. You can get this under the options in Profile settings.

**API Password** The API password provided by Paypal. You can get this under the options in Profile settings.

**API Signature** The unique signature provided by Paypal. You can get this under the options in Profile settings.

**Enable PSD2 for UK customer** The UK Customers require additional authentication, hence enter the PSD2 for the same.

**Message version** Please enter the message version in case if it is changed in feature.

**Processor ID** Enter process id associated with your CardinalCommerce account

**Merchant ID** Enter merchant id associated with your CardinalCommerce account

**Transaction Password** Enter transaction password associated with your CardinalCommerce account

**Card Types** Select the allowed card types for your store. Paypal has some regional differences. In USA< it accepts all card types, while in Canada only Visa and Mastercard are accepted. Check the regional differences here: \<link-text url ="https://developer.paypal.com/docs/classic/paypal-payments-pro/integration-guide/WPWebsitePaymentsPro/#id25a6cc16-bbc4-4070-a575-9fad358f2b95” target = “\_blank”rel = “noopener”> click here

**Payment Action** Set the type of payment you wanted to take. The default and RECOMMENDED setting is Sale. This will enable you to get the payment instantly credited to your account.

**Authorization:** An authorization payment action represents an agreement to pay and places the buyer’s funds on hold for up to three days. Choose this payment action if you need to ship the goods before capturing the payment or if there is some reason not to accept the payment immediately. After shipping, you have to login to your Paypal account and manually capture the payment.

**Use Paypal Sandbox** Set this to yes if you want to test the integration with a Paypal Sandbox account. To create a sandbox account you need to sign up for it athttp://developer.paypal.com” target = “\_blank”rel = “noopener”> click here

**Geozone** By selecting a geozone here, you can restrict this payment method from showing to customers from only that geo-region. Choose All geozones to show this method to all customers

**Refund Status** By when refund action processed in order page, then the order status will be changed to whatever order status you have set here.

**Geozone** By selecting a geozone here you can restrict this payment method from being shown to customers of only that geo-zone/region. Choose all geozone to show this payment method to all customers.

**Article ID for Thanks Message** You can create an article and enter its ID here to show to the customer after the transaction is completed.

**Display Text on Selection** The text entered here will be displayed when customer selects this payment method. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the tips below.

Tip - ONLY FOR MULTI-LINGUAL SITES

For example, enter a language constant:

J2STORE\_TEXT\_TO\_DISPLAY\_ON\_SELECTION

Now you can go to Joomla admin-> Language Manager->Overrides and create overrides for the language constant in all your languages.

**Display Text before Payment** The text entered here will be displayed to the customer at the order summary screen before he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text after Payment/Order** The text entered here will be displayed to the customer after he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text on Error in Payment** The text entered here will be displayed to the customer when there is an error in the payment process. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text on Cancel Payment** The text entered here will be displayed to the customer when he cancels the payment at the gateway (NOT in your site). You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Payment Button Text** The text of the payment button. The button will be displayed at the final checkout step.

**Support** Still have questions? You can post your questions in our support forum: [click here](http://j2store.org/forum/index.html)
