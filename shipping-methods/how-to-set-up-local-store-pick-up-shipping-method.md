# How to set up local store pick up shipping method

Many a times you might want to display a Store pickup option in the shipping method selection area of your site. Here is how it can be done.

## Methods: <a href="#methods" id="methods"></a>

There are two ways in which the local store pick up method could be shown on the store front.

1. Renaming the free shipping.
2. Creating a shipping method using the standard shipping method.

### Renaming the free shipping: <a href="#renaming-the-free-shipping" id="renaming-the-free-shipping"></a>

**Ideal for:** The following method is ideal when you don’t intend to use the free shipping plugin for other purposes.

**Procedure:**

* Navigate to Component > J2Commerce > Setup > Shipping methods > Free shipping.

![freeshippping](../.gitbook/assets/free-shipping-name-change.webp)

* Click on the View option.
* Rename the plugin’s display name to Local store pick up.

![renametolocalpickup](../.gitbook/assets/free-shipping-name-change1.webp)

* Save the changes.
* Now the free shipping would appear as Local store pick up at the frontend for users who choose the USA region at their address.

![freeshippingaslocalstore](https://raw.githubusercontent.com/j2store/doc-images/master/shipping-methods/how-to-set-up-local-store%3Dpick-up/local-store-image3.png)

**Video Tutorial:**

{% embed url="https://youtu.be/vYlO4qW-xL8" %}

## Creating a shipping method using the Standard shipping method: <a href="#creating-a-shipping-method-using-the-standard-shipping-method" id="creating-a-shipping-method-using-the-standard-shipping-method"></a>

**Ideal for:**

This process is ideal when you wish to use the Free shipping for other purposes but wish to display a store pickup option to users of a certain region.

**Procedure:**

* Navigate to Components > J2Commerce > Setup > Shipping methods  > Standard shipping methods.
* Click on the View option.

<figure><img src="../.gitbook/assets/standard-shipping.webp" alt=""><figcaption></figcaption></figure>

* Click on the New option.

![standardshippingmethod](../.gitbook/assets/standard-shipping-new.webp)

* Set the name as Store pick up and define the other conditions, if any

![setthedisplayname](../.gitbook/assets/standard-shipping-new1.webp)

* Click save and close.
* Click on the set rates button next to the newly created shipping method.

![setrates](../.gitbook/assets/standard-shipping-new2.webp)

* Choose the geozone (you will have to create one already in Components > J2Commerce > Localisation > Geozones) for which this shipping option should be available.

<figure><img src="../.gitbook/assets/standard-shipping-geozone.webp" alt=""><figcaption></figcaption></figure>

* Set the rate as 0.
* Click on the create button.

![geozone](../.gitbook/assets/standard-shipping-geozone1.webp)

* Now the frontend would show the shipping method for users of the chosen region.

![frontend](https://raw.githubusercontent.com/j2store/doc-images/master/shipping-methods/how-to-set-up-local-store%3Dpick-up/local-store-image8.png)

**Video tutorial:**

{% embed url="https://youtu.be/enjbI42xbt0" %}
