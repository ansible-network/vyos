====================
Ansible Network vyos
====================

.. _Ansible Network vyos_v2.6.0:

v2.6.0
======

.. _Ansible Network vyos_v2.6.0_Major Changes:

Major Changes
-------------

- Initial release of the ``vyos`` Ansible role.

- This role provides functions to perform automation activities on VyOS devices.


.. _Ansible Network vyos_v2.6.0_New Functions:

New Functions
-------------

- NEW ``get_facts`` function can be used to collect facts from VyOS devices.

- NEW ``config_manager/get`` function returns the either the current active or current saved configuration from VyOS devices.

- NEW ``config_manager/load`` function provides a means to load a configuration file onto a target device running VyOS.

- NEW ``config_manager/save`` function saves the current active (running) configuration to the startup configuration.

