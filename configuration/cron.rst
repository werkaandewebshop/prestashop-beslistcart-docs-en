Auto import
===========

On the module configuration page you can click on `view advanced options', there is a link to a script that performs a synchronization.

The link contains a secret key, so that only you can call the synchronization. The url looks like:

.. sourcecode:: bash

    http://www.yourdomainname.com/modules/beslistcart/cron.php?secure_key=YOUR_SECURE_KEY

It is highly recommended to set up a cron task that calls this script every 15 minutes. Running the script is a light task, and can therefore often happen. You can create a cron task such as:

.. sourcecode:: bash

    */10 * * * * curl --silent http://www.yourdomainname.com/modules/beslistcart/cron.php?secure_key=YOUR_SECURE_KEY &> /dev/null

This task retrieves new orders from Beslist.nl every 10 minutes.
