.. open-stack_

OpenStack
#########

.. code-block:: bash

    sudo -H pip install python-<product>client

Nova
====

* ``nova list``
* ``nova image-list``
* ``nova flavor-list``
* ``nova keypair-list``

Launch instance
---------------

.. code-block:: bash

    nova boot --flavor <flavor_num> --key_name <keypair_name>
        --image <image_id> <instance_name>

Filter `nova` output:

.. code-block:: bash

    nova boot ... | grep " <field> " | cut -d'|' -f3 | tr -d ' '

Terminate instance
------------------

.. code-block:: bash

    nova delete  (<instance_name>|<instance_id>)

Get instance IP
---------------

.. code-block:: bash

    nova interface-list (<instance_name>|<instance_id>) | grep 'ACTIVE' | \
        cut -d'|' -f5 | tr -d ' '
