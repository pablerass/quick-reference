.. aws_

AWS
###

`AWS Command Line Interface Documentation <http://aws.amazon.com/es/documentation/cli/>`_

Install aws client
==================

.. code-block:: bash

    pip install awscli

Upload certificate to AWS
=========================

.. code-block:: bash

  aws iam upload-server-certificate --server-certificate-name <name>
      --private-key file://<name>.key --certificate-body file://<name>.pem
      --certificate-chain file://<chain_name>.pem --path <path>

If the certificate will be used inside *CloudFront* the path has to be
`/cloudfront/<name>/`.

.. warning::

  Amazon only support *pem* format uploads. Instrucctions about how to convert
  from different formats are listed in certificates_ section.

Certificates can be listed with the following command:

.. code-block:: bash

  aws iam list-server-certificates

More information can be obtained in the following links:

  * `Using an HTTPS Connection to Access Your Objects <http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/SecureConnections.html>`_
  * `SSL Certificates for Elastic Load Balancing <http://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/ssl-server-cert.html>`_

