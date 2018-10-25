Module configuration
===================
The module configuration can be found in your Prestashop installation. Navigate to `Modules` ->` Modules and Services`, search for the `Beslist Shopping cart integration` module and click on` Configure`.

Configure the test connection
-----------------------------
It is highly recommended to first configure a test connection. From Beslist you (if it is correct) have received the data for a test connection. Even when you are running in another system, it is important to first use the Test API keys.

***Make sure you use the Test API keys for the test connection***

Configuration options
-------------------
Here you will find a brief explanation for each configuration option.

Beslist productfeed settings
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The settings under the heading 'Decisive product feed settings' only apply to the product feed functionality of the module.

* `Standard size attribute`: If your products use different sizes, you can enter it here.
* `Standard color attribute`: If your products use different colors, you can enter it here.
* `Use longe descriptions in feed`: If `YES` your long description is passed to Beslist, by default the feed uses the short product description.
* `Beslist productreference field`: Here you indicate which field is used as a unique field. If it is good, you have passed it on Decidedly. By default, the module uses a combination of the Prestashop ID of the product and the product combination ID (this field is also used in the feed, and works with Channable). The other options are EAN-13 (barcode) and Productreference (your internal reference). In most cases the standard works, so always try first.
* `Filter products without stock`: Do not include products in the feed that do not have inventory.

Beslist.nl settings
^^^^^^^^^^^^^^^^^^^^^^^
These settings only apply to the publications on Beslist.nl, the Dutch website.

* `Use Beslist.nl`: Synchronize orders and products with Beslist.nl (Netherlands).
* `Carrier`: Select a carrier for your Dutch orders. The order and transport costs must match (on Beslist.nl and in your Prestashop carrier configuration).
* `Delivery period`: The delivery time for Dutch orders for which the products are in stock.
* `Delivery period no stock`: The delivery time for Dutch orders for which the products are not in stock.

Beslist.be settings
^^^^^^^^^^^^^^^^^^^^^^^
These settings only apply to the publications on Beslist.be, the Belgian website.

* `Use Beslist.be`: Synchronize orders and products with Beslist.be (Belgium).
* `Carrier`: Select a carrier for your Belgian orders. The order and transport costs must match (on Beslist.be and in your Prestashop carrier configuration).
* `Delivery period`: The delivery time for Belgian orders for which the products are in stock.
* `Delivery period no stock`: The delivery time for Belgian orders for which the products are not in stock

Beslist Shopping cart settings
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The settings under the heading `Beslist shopping cart settings' apply to both Beslist.nl and Beslist.be.

* `Enable Beslist Shopping cart`: Enable or disable the Beslist shopping cart functionality for this website
* `Shop ID`: The Shop ID you received from Beslist.
* `Client ID`: The Client ID that you received from Beslist.
* `Order API key`: The personal Order API key that you received from Beslist.
* `Shopitem API key`: The key you received for the Shop Item API.
* `Gebruik testverbinding`: Activate the Test APIs
* `Test productnummer`: Here you fill in the code ('$combinationID-$productid', EAN-13 or product reference) of the product you want to use during the test. The completed code must match the `Beslist product reference field` field.
     * Standard: a combination of the product and combination ID of the product (#combination-#product). Example:
         * `3-4` Product ID: 4, Combination ID: 3 (visible in the url and database,`id_product` & `id_product_attribute`)
         * `4` Product ID: 4, no combination (visible in the url and database,` id_product`)
     * EAN-13: The EAN code of the product (visible on the product page)
     * Product reference: The product reference of the product (visible on the product page)
* `From date`: The date from when orders are to be synchronized. This field is automatically updated after a synchronization.
* `House number in address2`: Shows the home number in a separate field.

Bulk operations
^^^^^^^^^^^^^^^
Here you can choose to

* `Add all products` - Marks all products for the Beslist feed
* `Add standard categories` - Put the Beslist.nl categories in a best effort way on the products
* `Mark 1000 as updated` - Marks 1000 products so that they can be reported via the Shopitem API.

Categories
^^^^^^^^^^
The Beslist categories are saved in your PrestaShop installation, so that you can select the category for each product. You can retrieve the categories from Beslist by setting `Update Beslist categories' to` YES`, and then clicking on save.

* `Update Beslist categories': Refresh the local list of categories of Beslist
* `Default category`: Select a default category for your products. For more information about categories you can look at the :doc:`categories page <usage/categories>`_

Live connection
^^^^^^^^^^^^^^^
After you have configured the test connection and performed the tests correctly, you can configure the module for production mode. For that only a few fields need to be changed:

* 'Use test connection': Set this field to 'NO'
* `Shopitem API key`: Your Shopitem API key

You are now ready to receive orders. Read in the :doc:`user documentation <usage/orders>`_ how this works.
