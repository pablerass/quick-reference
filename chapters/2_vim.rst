.. vim_

Vim
###

Basic configuration
===================

* Show line numbers:

.. code-block:: bash

    :set number

* Enable syntax highlighting:

.. code-block:: bash

    :syntax on

* Enable and disable line wrapping:

.. code-block:: bash

    :set wrap
    :set nowrap

* Use spaces instead of tabs

.. code-block:: bash

    :set expandtab

Copy and paste
==============

Use buffers
-----------

* ``"<buf>y``
* ``"<buf>p``
* ``"<buf>d``

System clipboard ``+`` buffer - ``"+(y|p|d)``

.. note::

    ``*`` should be also be used in Linux and Windows, but it does not work in
    my system.

Examples
--------

* ``gg"+yG`` Copy all text into the system clipboard.

Run scripts
===========

* ``:!%`` or ``:! sh %`` if you do not have run privileges.

Check spelling
==============

* ``[s`` ``]s`` - Go to the following or previous error.

* ``=z`` - Show recomendations

Enable and disable spelling check
---------------------------------

`my dotfiles <https://github.com/pablerass/dotfiles>`_

* ``,NC``
* ``,CE``
* ``,CS``
* ``,CF``

Special symbols
===============

``<ctrk>k`` and it *digraph* combination.

``:digraph``

======== =========
*Symbol* *Digraph*
±        ``+-``
∼        ``?1``
≈        ``?2``
≠        ``!=``
≤        ``=<``
≥        ``>=``
∞        ``00``

α        ``a*``
β        ``b*``
δ        ``d*``
λ        ``l*``
π        ``p*``

∀        ``FA``
∃        ``TE``
∧        ``AN``
∨        ``OR``

Ø         ``O/``
∈        ``(-``
∋        ``-)``
∩        ``(U``
∪        ``U)``
⊂        ``(C``
⊃        ``C)``
⊆        ``(_``
⊇        ``)_``
======== =========
