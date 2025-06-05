---
description: J2Commerce (formerly known as J2Store)
---

# Setting up tax for your products

## Requirement for the tax to take effect: <a href="#requirement-for-the-tax-to-take-effect" id="requirement-for-the-tax-to-take-effect"></a>

* Geozone has to be set up for which the tax has to apply.
* Tax rate has to be set up.
* Tax profile has to be created.
* Tax rate has to be associated with the tax profile.
* Tax profile has to be assigned to the products for which tax has to be levied.

## Instance: <a href="#instance" id="instance"></a>

Tax geozone: USA

Tax rate: 10%

Tax profile name: US-TAX

**Steps:**

* Navigate to J2Commerce > Localisation > Geozones and create a new geozone.

![Creating a new geozone](../.gitbook/assets/tax_geo_zone.webp)

* Type in a name for the geozone, add the countries for which the tax has to be applied.
* Case A: Apply tax only for few zones within USA.

![Filling in details on the newly created geozone](../.gitbook/assets/tax_geo_zone1.webp)

2\. Case B: Apply tax for all zones within USA.

![Adding country](../.gitbook/assets/tax_geo_zone2.webp)

Navigate to J2Commerce > Localisation > Tax rates > Click new.

![](../.gitbook/assets/tax_rate.webp)

Fill in the name, tax percentage, geozone and publish the tax rate.

![](../.gitbook/assets/tax_rate1.webp)

Navigate to J2Commerce > Localisation > Tax profile > New.

![](../.gitbook/assets/tax_profile.webp)

Fill in the profile name, set the status and map the tax rate on the profile, choose the associated address.

![Adding details to tax profiles](../.gitbook/assets/tax_profile1.webp)

Navigate to J2Commerce > Catalog > Products (Or Content > Articles).

![](../.gitbook/assets/product_list.webp)

Edit the products for which you wish to collect tax. Navigate to the J2Commerce (J2Store Cart) tab. Choose the tax profile and save.

![](../.gitbook/assets/tax_rate2.webp)

Frontend:

![](../.gitbook/assets/setting-tax-front.png)

![](../.gitbook/assets/setting-tax-in-cart-page.png)

Thus tax would be levied on the product as per the configuration.

### Issues: <a href="#issues" id="issues"></a>

Please refer the following list of troubleshooting steps:

[click here](https://docs.j2store.org/catalog/setting-up-tax-for-your-products/\[http://docs.j2store.org/troubleshooting-guide/troubleshooting-tax-issues]\(%3Chttp:/docs.j2store.org/troubleshooting-guide/troubleshooting-tax-issues%3E\))
