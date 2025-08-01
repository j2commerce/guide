---
description: J2Commerce (formerly known as J2Store)
---

# Braintree payment plugin

This plugin integrates the Braintree payment gateway with J2Commerce.

You need an account with Braintree to choose this method. If you have/create one, you will be provided with the Merchant ID, private, and public keys for facilitating payments. You need to enter them in the respective fields. In these payment types, unlike Bank Transfer or Money order methods, the customer has the option to cancel the payment. Also, if any error occurs during the payment process, it will be logged. These will be notified through the additional text boxes provided

**Step 1:**  Purchase:

Go to > J2commerce > App > Braintree > Add to Cart.&#x20;

<figure><img src="../.gitbook/assets/braintree-purchase.webp" alt=""><figcaption></figcaption></figure>

**Step 2:** Download:&#x20;

After you purchase the App, it will be in your “My Downloads” section. Go to your profile icon in the upper right corner > My downloads > Search “Braintree” > Available Versions

<figure><img src="../.gitbook/assets/braintree-download-1.webp" alt=""><figcaption></figcaption></figure>

Next, go to View Files > Download the latest version > save it in a location you will remember

<figure><img src="../.gitbook/assets/braintree-download.webp" alt=""><figcaption></figcaption></figure>



**Step 3:** Installation:

Go to System > Install > Extensions > Upload Braintree zip file. &#x20;

<figure><img src="../.gitbook/assets/braintree-install (1).webp" alt=""><figcaption></figcaption></figure>

**Step 4:** Publish:

Make sure you enable the App.  Go to J2Commerce > Setup > Payment Methods > Find Braintree and click Enable

<figure><img src="../.gitbook/assets/braintree-enable.webp" alt=""><figcaption></figcaption></figure>

**Step 5:** Log in to your Braintree account to locate your Braintree Credentials. &#x20;

If you already have a Braintree account but are not sure where to find the relevant credentials (Merchant ID, Public Key, Private Key, and Merchant Account ID), follow the steps below.

**To locate your Braintree credentials:**

* [Sign in](https://www.braintreegateway.com/login) to your Braintree account.
* Click My User under Account.
* Click View API Keys.
* Click View under Private Key.
* Copy the following values:&#x20;
  * Public Key
  * Private Key
  * Merchant ID
* Click Processing under Settings.
* Find your default merchant account in the Merchant Accounts section.\
  Note: In most cases, there is only one merchant account.
* Copy the Merchant Account ID (copy the ID only, without "default").

Once you have located your credentials, you can enter them in the backend of your site.&#x20;

**Configuration:**

Payment Option title:

Enter a name that will be shown in the payment methods selection during the checkout process. \*\*Default Braintree\*\*

**Plugin Display Image:**

Select the image of the plugin that you wish to display on the frontend.

<figure><img src="../.gitbook/assets/braintree1 (1).webp" alt=""><figcaption></figcaption></figure>

**Live Merchant ID:** Enter your live account’s Merchant ID Key.

**Live Private Key:** Enter your live account’s Private API Key.

**Live Public Key:** Enter your live account’s Public API Key

**Test Merchant Account List:** The merchant details will be displayed after entering the Merchant key, public key, and private key, and then clicking on save.

**Use sandbox:** This option allows you to test the plugin with Paymill in test mode instead of the live one.

To log in to your Sandbox account, go to the Sandbox link at the bottom under the Braintree login button

**\*\*IMPORTANT:** NEVER set this to yes when your shop is live.

**Test Private Key:** Enter your test Private API Key here.

**Test Public Key:** This is the test public key to be used while testing the payment plugin. You can find these keys under your account settings.

**Test Merchant Account list:** The merchant details will be displayed after entering the test merchant key, test public key, test private key, and clicking on save

**Payment Type:** Choose the desired payment type according to the requirement.

<figure><img src="../.gitbook/assets/braintree2.webp" alt=""><figcaption></figcaption></figure>

**Sandbox:** The following images show you where to find your merchant ID and API Key once you're logged into your Sandbox Account

<figure><img src="../.gitbook/assets/sandbox-braintreegateway-merchants1.webp" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/sandbox-braintreegateway-merchants2.webp" alt=""><figcaption></figcaption></figure>

**Display text on selection:**

The text entered here will be displayed when the customer selects this payment method. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer to the tips below

Tip - ONLY FOR MULTI-LINGUAL SITES

**For example, enter a language constant:**

J2STORE\_TEXT\_TO\_DISPLAY\_ON\_SELECTION.

Now you can go to Joomla! admin > Language Manager > Overrides and create overrides for the language constant in all your languages.

**Display text before payment:**

The text entered here will be displayed to the customer at the order summary screen before they make the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer to the Display text on the selection parameter.

**Display text after payment/order:**

The text entered here will be displayed to the customer after he makes the payment. You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer to the Display text on the selection parameter.

**Display text on error in payment:**

The text entered here will be displayed to the customer when there is an error in the payment process.

You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer to the Display text on the selection parameter.

**Display text on cancel payment:**

The text entered here will be displayed to the customer when they cancel the payment at the gateway (NOT in your site).

You can enter a language constant as a value here if you are using a multi-lingual site and then write a language override. Refer to the Display text on the selection parameter.

**Payment Button Text:**

The text of the payment button. The button will be displayed at the final checkout step.

Debug Mode: Setting debug mode to yes will allow errors to be logged in case of transaction failures.

**Support:** Still have questions? You can contact us directly at: [https://www.j2commerce.com/support](https://www.j2commerce.com/support)

Thank you for using our extension.

\
