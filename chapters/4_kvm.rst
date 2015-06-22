.. kvm_

KVM
###

.. code-block:: bash

    qemu-img create hdd.vdi 10G
    kvm -hda hdd.vdi -cdrom ubuntu-14.04.2-server-amd64.iso -m 512 -net nic -net user -curses -nographic
