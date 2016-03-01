.. certificates_

Certificates
############

Convert to PEM
==============

.. code-block:: bash

    openssl x509 -inform PEM -in <name>.cer -out <name>.pem

Covert from pkcs12
==================

Convert to *pem* format without passphrase:

.. code-block:: bash

    openssl pkcs12 -in movil.bbva.es.p12 -nodes -out movil.bbva.es.pem

Export only the private key:

.. code-block:: bash

    openssl pkcs12 -nocerts -nodes -in movil.bbva.es.p12 -out movil.bbva.es.key

Export only the client certificate:

.. code-block:: bash

    openssl pkcs12 -nokeys -clcerts -in movil.bbva.es.p12 -out ca-certs.pem

Export only the CA certs:

.. code-block:: bash

    openssl pkcs12 -nokeys -cacerts -in movil.bbva.es.p12 -out ca-certs.pem

.. note::

    `-nodes` flag prevents using a passphrase to encrypt the private key.
