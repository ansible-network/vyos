====================
Ansible Network vyos
====================

.. _Ansible Network vyos_v2.7.2:

v2.7.2
======

.. _Ansible Network vyos_v2.7.2_New Tasks:

New Tasks
=========

- Added ``configure_lldp`` task `vyos-#44 <https://github.com/ansible-network/vyos/pull/44>`_.


.. _Ansible Network vyos_v2.7.2_Minor Changes:

Minor Changes
=============

- Update ``config_manager/load`` function to use cli_config `vyos-#48 <https://github.com/ansible-network/vyos/pull/48>`_.

- Implement ``replace`` functionality using cli_config and cli_command `vyos-#49 <https://github.com/ansible-network/vyos/pull/49>`_.

- Update ``load`` and ``replace`` tests `vyos-#50 <https://github.com/ansible-network/vyos/pull/50>`_.


.. _Ansible Network vyos_v2.7.1:

v2.7.1
======

.. _Ansible Network vyos_v2.7.1_New Tasks:

New Tasks
---------

- Added ``configure_vlans`` tasks `vyos-#34 <https://github.com/ansible-network/vyos/pull/34>`_.

- Added ``configure_system_properties`` task `vyos-#38 <https://github.com/ansible-network/vyos/pull/38>`_.


.. _Ansible Network vyos_v2.7.1_Bugfixes:

Bugfixes
--------

- Fixed compare functionality to exhibit correct behavior `vyos-#39 <https://github.com/ansible-network/vyos/pull/39>`_.

- Fixed ``configure_user`` task parameters `vyos-#33 <https://github.com/ansible-network/vyos/pull/33>`_.


.. _Ansible Network vyos_v2.7.0:

v2.7.0
======

.. _Ansible Network vyos_v2.7.0_Major Changes:

Major Changes
-------------

- Initial release of 2.7.0 ``vyos`` Ansible role that is supported with Ansible 2.7.0


.. _Ansible Network vyos_v2.6.2:

v2.6.2
======

.. _Ansible Network vyos_v2.6.2_Bugfixes:

Bugfixes
--------

- Fix parameters to align with config_manager role

- validate_role_spec to only consider config_manager_text parameter


.. _Ansible Network vyos_v2.6.1:

v2.6.1
======

.. _Ansible Network vyos_v2.6.1_Minor Changes:

Minor Changes
-------------

- Added minimum Ansible version check `vyos#19 <https://github.com/ansible-network/vyos/pull/19>`_.


.. _Ansible Network vyos_v2.6.1_New Parser Templates:

New Parser Templates
--------------------

- New Parser Template ``show_system_storage``


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

