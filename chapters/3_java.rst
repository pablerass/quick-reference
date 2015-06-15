.. java_

Java
####

Keytool
=======

* Add a Trusted Certificate to a keystore

.. code-block:: bash

    keytool -importcert -file <cert>.cer -keystore <keystore>

* List Trusted CA Certs

.. code-block:: bash

    keytool -list -v -keystore <keystore>

.. note::

    If `-keystore` parameter it is not specified, user `$HOME/.keystore`.
