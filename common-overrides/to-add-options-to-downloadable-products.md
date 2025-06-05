---
description: J2Commerce (formerly known as J2Store)
---

# To add options to downloadable products

Copy **/administrator/components/com**_**j2store/views/product/tmpl/form**_**downloadable.php** To **\*/administrator/templates/YOUR-DEFAULT-TEMPLATE/html/com**_**j2store/product/form**_**downloadable.php**

Find the below line

```
<li>
<a href="#imagesTab" data-toggle="tab"><i class="fa fa-file-image-o"></i>
<?php echo JText::_('J2STORE_PRODUCT_TAB_IMAGES'); ?>
</a>
</li>
```

Change with

```
<li>
<a href="#imagesTab" data-toggle="tab"><i class="fa fa-file-image-o"></i> <?php echo JText::_('J2STORE_PRODUCT_TAB_IMAGES'); ?>
</a>
</li>
<li>
<a href="#optionsTab" data-toggle="tab"><i class="fa fa-sitemap"></i> 
<?php echo JText::_('J2STORE_PRODUCT_TAB_OPTIONS'); ?>
</a>
</li>
```

Find below line

```
<div class="tab-pane" id="imagesTab">
<?php echo $this->loadTemplate('images');?>
</div>
```

Change with

```
<div class="tab-pane" id="imagesTab">
<?php echo $this->loadTemplate('images');?>
</div>
<div class="tab-pane" id="optionsTab">
<?php  echo $this->loadTemplate('options');?>
</div>
```

Save.

Copy /components/com\_j2store/templates/YOUR-SUB-LAYOUT/view\_downloadable.php

to /templates/YOUR-TEMPLATE/html/com\_j2store/templates/YOUR-SUB-LAYOUT/view\_downloadable.php

Edit the file and find below line

```
<?php echo $this->loadTemplate('cart'); ?>
```

Change with

```
<?php echo $this->loadTemplate('options'); ?>
<?php echo $this->loadTemplate('cart'); ?>
```

Save. Now the downloadable products should have options tab at the back end and the options should be visible on the front end.
