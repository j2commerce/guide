---
description: >-
  J2Commerce (formerly known as J2Store):  This plugin integrates USAePay
  payments with J2Store.
---

# USAePay Payment Plugin

## Requirements

1. PHP 8.1.0 +
2. Joomla! 4.x/ Joomla! 5.x +
3. J2Commerce / J2Store 4.x +

## Installation <a href="#installation" id="installation"></a>

1. Download the USAePay payment plugin package from our site’s extensions section and install it using Joomla installer.
2.  After installing plugin, go to J2Store > Setup > Payment methods and enable USAePay

    for J2Store.
3. Once enabled, open / edit the plugin and configure the basic settings of the app.

## Configuration <a href="#configuration" id="configuration"></a>

**Payment option title:** You may enter the title of the payment method you wish to display at the frontend in checkout here. If left blank, the default payment text will be displayed.

**Image or logo:** You may consider adding an image for the payment method to be listed in the checkout page next to the payment method in frontend.

**API Key:** Enter your USA E-PAY pin key associated with your USA E-PAY account.

**Pin:** Enter your USA E-PAY pin associated with your USA E-PAY account.

**Payment URL:** If you are using a production mode and do have any other alternate payment URL then you may enter it here.

**Use USA E Pay Sandbox:** This option allows you to set the USA E-PAY gateway using the USA E-PAY server instead of the live one. Use this option to test the plugin if you do not have a USA E-PAY account.

**Test API key:** Enter your USA E-PAY Test pin key associated with your USA E-PAY account.

**TEST PIN:** Enter your USA E-PAY Test pin associated with your USA E-PAY account.

**Geozone:** You can restrict showing this payment method only to the customers who belong to the selected geozone. Choose All in order to display this payment option to all customers.

![USA E-PAY Payment Img1](../.gitbook/assets/usa-e-pay-img1.png)

**Display Text on Selection:** The text entered here will be displayed when customer selects this payment method. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the tips below.

**Tip - ONLY FOR MULTI-LINGUAL SITES**

For example, enter a language constant:

J2STORE\_\_TEXT\_\_TO\_\_DISPLAY\_\_ON\_SELECTION

Now you can go to Joomla admin-> Language Manager->Overrides and create overrides for the language constant in all your languages.

**Display Text before Payment:** The text entered here will be displayed to the customer at the order summary screen before he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text after Payment:** The text entered here will be displayed to the customer after he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text on Error in Payment:** The text entered here will be displayed to the customer when there is an error in the payment process. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Display Text on Cancel Payment:** The text entered here will be displayed to the customer when he cancels the payment at the gateway (NOT in your site). You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer the Display text on selection parameter.

**Payment Button Text:** The text of the payment button. The button will be displayed at the final checkout step.

**DEBUG :** This option is chosen in order to enable or disable the display of log file. This should be in disable for live sites.

Thus, once you have mentioned the necessary details for the above parameters, you are ready to receive payments via USA E-PAY on your store.

![USA E-PAY Payment Img2](../.gitbook/assets/usa-e-pay-img2.png)
