.. apt

Apt
###

Package sign
============

Generate key pair
-----------------

.. code-block:: bash

    gpg --gen-key

Export public key in text mode
------------------------------

.. code-block:: bash

    gpg --export --armor 70B01383 > artifactory.asc

Export and import private key
-----------------------------

.. code-block:: bash

    gpg --export-secret-keys 70B01383 > artifactory.key
    gpg --allow-secret-key-import --import artifactory.key

Sign deb package
----------------

.. code-block:: bash

    debsigs --sign=archive -k 70B01383 git_2.6.3-0ppa1-ubuntu14.04.1_amd64.deb

