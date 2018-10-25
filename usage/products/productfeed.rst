Productfeed
===========

The module has a possibility to generate a feed. The generator must be set via cron.
An example of a command can be found on the module configuration page (under 'View advanced options').

For instance:

.. sourcecode:: bash

    0 1 * * * curl -L --max-redirs -1 https://www.uwdomeinnaam.nl/modules/beslistcart/cron-generate.php?secure_key=XXXYYY111222333  &>/dev/null

This task will run at 1:00 every night. Depending on the number of products, the task may take a long time. You can also use an external feed. It is known that the module works well with `Channable <http://www.channable.com>`_. You have more control over your feed via an external party.
