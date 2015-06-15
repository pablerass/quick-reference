.. system

System
######

Process
=======

.. code-block:: bash

    ps -xua

Networking
==========

Listening ports
---------------

.. code-block:: bash

    netstat -antop | grep LISTEN

Routing
-------

.. code-block:: bash

    sudo route remove default gw && sudo route add default gw <ip>

Packet filtering
----------------

tcpdump
*******

.. code-block:: bash

    clear && tcpdump -nnS[vvv] <filter>

* `-n` - Don’t resolve hostnames.
* `-nn`  - Don’t resolve hostnames or port names.
* `-v`, `-vv`, `-vvv` - Increase the amount of packet information you get back.
* `-S` - Print absolute, rather than relative, TCP sequence numbers.
