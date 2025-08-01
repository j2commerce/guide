---
description: >-
  How to customize product views when using Joomla article short codes with
  J2Commerce (formerly known as J2Store).
---

# Customizing Article Short Codes

If you are using the Joomla article category views in your project and wish to have more control over the display of your J2Commerce products, follow the steps below:

TAKE A FULL SITE BACKUP BEFORE THESE STEPS TO AVOID ISSUES!

**Front End View**



Create Layout Override Folder

```
templates/<template>/html/com_j2store/product
```

Copy Files From:

```
components/com_j2store/views/product/tmpl
```

To

```
templates/<template>/html/com_j2store/product
```

**Example:** If you wish to have downloadable products display product options (after following the [Add Options to Downloadable Products](to-add-options-to-downloadable-products.md) instructions):

```
templates/<template>/html/com_j2store/product/item_downloadable.php
```

**Find the line shown below:**

```
<?php echo $this->loadTemplate('cart'); ?>
```

**BEFORE that line, insert a new line and with the following:**

```
<?php if($this->product->has_options): ?>
  <?php echo $this->loadTemplate('options'); ?>
<?php endif; ?>
```

**Final Result:**

```
<?php if($this->product->has_options): ?>
  <?php echo $this->loadTemplate('options'); ?>
<?php endif; ?>
<?php echo $this->loadTemplate('cart'); ?>
```

**Save File:**

```

templates/<template>/html/com_j2store/product/item_downloadable.php
```

If you now look at a Downloadable Product displayed using a Short Code, you should see any options set for that product in the display.

Now the downloadable products should display any options that were added to the product in the frontend Short Code display.
