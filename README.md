# Kelkoogroup Sales Tracking for Magento2 

Track your orders in Kelkoo.


## Implement the lead tag

* If you want to add Kelkoogroup leadtag without creating a module, you can add the following code on your active theme.
```
// YourTheme/Magento_Theme/layout/default_head_blocks.xml
<script src="https://s.kk-resources.com/leadtag.js" src_type="url"/>
```

## Implement the conversion tag

1. Under your magento installation create directory app/code/ if it’s missing
2. go to /app/code
3. Download Kelkoost_magento2-2.zip module for magento 2. (compatible for Magento 2.2 and 2.3)
4. copy Kelkoost_magento2-2.tgz in directory /app/code
5. extract Kelkoost_magento2-2.tgz
6. check directory tree, you should have something similar to: 
```
app/code/Kelkoo/Modulekelkoost/   
|- Block   
|    |- Success.php   
|- etc   
|    |- di.xml   
|    |- module.xml   
|- registration.php   
|- view   
|    |- frontend   
|    |     |-  layout   
|    |     |     |- checkout_onepage_success.xml   
|    |     |-  templates   
|    |     |     |- checkout   
|    |     |     |     |- success.phtml 
```
7. Modify file app/code/Kelkoo/Modulekelkoost/view/frontend/templates/checkout/success.phtml to set the correct country and comid

8. Enable kelkoost module :
```
php bin/magento module:enable Kelkoo_Modulekelkoost 
php bin/magento setup:upgrade --keep-generated 
```

