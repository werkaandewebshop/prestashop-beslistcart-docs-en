Categories
===========
From version 1.3.0 there is more extensive support for the categorization of Beslist. In addition to your own categorization, it is possible to send a predefined Beslist mapping with the products. This can be done on 3 levels: shop, shop category and product.

Beslist internal mapping
-----------------------

The default category of each product is included in the feed. On the basis of this categorization, Beslist creates a mapping to their own categories. So in principle you do not have to do anything to get the products in the right categories.

Your own mapping
----------------

** The steps below are not necessary for most cases, in consultation with Beslist will see if you can create your mapping yourself **

Categorization at shop level
^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can specify on the module configuration page which default category to use for Beslist. This will be included if no other match is possible.

Categorization on shop category
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In your Prestashop environment you can go to `Catalog` -> `Categories`. Select the category for which you want to set a Beslist category. On the edit page there is a field `Beslist category`. This category will be used when there is no match at product level.

The matching on shop category works through the entire tree of your shop. So if you have set a Beslist category at a higher level, it will be used.

Categorization at product level
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you can not indicate which category corresponds to the product on the shop and shop category level, you can indicate a category for the product on the product page itself. This category will always be included in the feed.

Determination method per product
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the feed a corresponding category is searched per product, this works as follows:

1. If a Beslist category is entered for the product, the feed uses it
2. If a Beslist category is entered for the (main) category of the product, the feed uses it
3. If a Beslist category is found in the parent categories of the product, the feed uses it
    - We look at which category is the deepest, so it may be that the main category of the product is not used, but another category where the product is also.
4. If there is still no match available, the default category of the shop is used in the feed
