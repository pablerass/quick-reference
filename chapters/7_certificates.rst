.. certificates_

Certificates
############

Convert to PEM
==============

.. code-block:: bash

    openssl x509 -inform PEM -in <name>.cer -out <name>.pem

Check certificate
=================

.. code-block:: bash

    openssl verify -purpose sslserver -CAfile <chain_name>.pem <name>.pem

Covert from pkcs12
==================

Convert to *pem* format without passphrase:

.. code-block:: bash

    openssl pkcs12 -in <name>.p12 -nodes -out <name>.pem

Export only the private key:

.. code-block:: bash

    openssl pkcs12 -nocerts -nodes -in <name>.p12 -out <name>.key

Export only the client certificate:

.. code-block:: bash

    openssl pkcs12 -nokeys -clcerts -in <name>.p12 -out <name>.pem

Export only the CA certs:

.. code-block:: bash

    openssl pkcs12 -nokeys -cacerts -in <name>.p12 -out <chain_name>.pem

.. note::

    ``-nodes`` flag prevents using a passphrase to encrypt the private key.
