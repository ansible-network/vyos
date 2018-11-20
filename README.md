# vyos

This Ansible Network role provides a set of platform dependent fuctions that
are designed to work with VyOS network devices.  The functions included
in this role inlcude both configuration and fact collection.

## Requirements

* Ansible 2.6 or later
* Ansible Network Engine Role 2.6.0 or later

## Functions

This section provides a list of the availabe functions that are including
in this role.  Any of the provided functions can be implemented in Ansible
playbooks to perform automation activities on VyOS devices.

Please see the documentation link for each function for details on how to use
the function in an Ansible playbook.

* get_facts [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/get_facts.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/get_facts.md)
* configure_sys_props [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/configure_sys_props.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/system_properties.md)

### Config Manager

* config_manager/get [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/config_manager/get.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/config_manager/get.md)
* config_manager/save [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/config_manager/save.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/config_manager/save.md)
* config_manager/load [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/config_manager/load.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/config_manager/load.md)

### Cloud VPN
* cloud_vpn/configure_vpn_initiator [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/cloud_vpn/configure_vpn_initiator.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/cloud_vpn/configure_vpn_initiator.md)
* cloud_vpn/configure_routing_initiator [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/cloud_vpn/configure_routing_initiator.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/cloud_vpn/configure_routing_initiator.md)
* cloud_vpn/configure_vpn_responder [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/cloud_vpn/configure_vpn_responder.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/cloud_vpn/configure_vpn_responder.md)
* cloud_vpn/configure_routing_responder [[source]](https://github.com/ansible-network/vyos/blob/devel/tasks/cloud_vpn/configure_routing_responder.yaml) [[docs]](https://github.com/ansible-network/vyos/blob/devel/docs/cloud_vpn/configure_routing_responder.md)

## License

GPLv3

## Author Information

Ansible Network Community
