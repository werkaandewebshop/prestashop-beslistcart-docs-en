Beslist.nl configuration
=======================

The Beslist.nl configuration has to be setup at your `Beslist.nl account <https://cl.beslist.nl/v2/user/login>`_

Shopping cart settings
------------------------
The module supports 1 way of calculating shipping costs, namely the option 'The order costs are calculated on the basis of the total turnover of the order (s).'.
Set this as an option on Beslist.nl (for both Belgium and the Netherlands). You do this on the page `Shopping cart` ->` Settings`. Make sure the specification matches the calculation of the shipping costs within your Prestashop installation. You can choose to create a new carrier, where the settings correspond exactly to the settings on Beslist.

API keys
------------
The module uses multiple Beslist API's. Namely:

1. Order API
2. Shopitem API

For this it is necessary to obtain API keys. You will receive these from Beslist via email.

Test API
--------
Initially, a key is provided for the test environment of the Shop Item API. The Order API always uses the production environment, but can be tested in a different way.

After you have made a number of successful Shop Item API notifications, you can receive a production API key from Beslist.

Note: the module can only be put into test mode in its entirety, if you want to use the Order API already, keep in mind that the Shopitem API does nothing.
