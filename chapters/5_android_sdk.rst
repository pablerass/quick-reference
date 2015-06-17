.. android_sdk_

Android SDK
###########

Manage SDK components
=====================

List all targets:

.. code-block:: bash

    android list targets

Manage AVDs
-----------

List all AVDs:

.. code-block:: bash

    android list avd

Create an AVD:

.. code-block:: bash

    android create avd -n <avd_name> -t android-22 --abi default/x86_64

Created AVDs are stored in ``$HOME/.android/avd`` directory.

Install and update components
-----------------------------

Update all system images:

.. code-block:: bash

    android update sdk --no-ui --all --filter system-image

Emulators
=========

.. code-block:: bash

    emulator-x86 -avd <avd> [-qemu -m <mem> -enable-kvm]

Install KVM emulation
---------------------

``kvm-ok``

.. code-block:: bash

    apt-get install libsdl1.2debian:i386 libgl1-mesa-dev:i386
    apt-get install qemu-kvm libvirt-bin bridge-utils
    apt-get install ubuntu-vm-builder virt-manager

.. note::

    Some of this packages may not be required.

Connect to Android devices
==========================

Connection to emulated device
-----------------------------

* ``adb connect <ip>``
* ``adb devices``
* ``adb disconnect <ip>``

Root privileges and shell access
--------------------------------

* ``adb root``
* ``adb shell``

Application management
----------------------

* ``abd install <app_apk_file>``
* ``adb uninstall <app_install_name>``

Applications are installed in ``/data/app`` or ``/data/app-private``.

.. warning::

    In order to run ADB or AAPT on *Ubuntu Linux 14.04 x86_64*, the following
    packages must be installed:

    .. code-block:: bash

        sudo apt-get install libc6:i386 libstdc++6:i386 zlib1g:i386