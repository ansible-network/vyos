# Configure LLDP on the device

The `configure_lldp` function can be used to set LLDP on VyOS devices.
This function is only supported over `network_cli` connection type and 
requires the `ansible_network_os` value set to `vyos`.

## How to set LLDP on the device

To set LLDP on the device, simply include this function in the playbook
using either the `roles` directive or the `tasks` directive.  If no other
options are provided, then all of the available facts will be collected for 
the device.

Below is an example of how to use the `roles` directive to set LLDP on the 
VyOS device.

```
- hosts: vyos

  roles:
  - name ansible-network.vyos
    function: configure_lldp
  vars:
    lldp:
      - interface_location: all
        interface: eth0
        legacy_protocols: cdp
        management_address: 192.168.1.1
        snmp: true
```

The above playbook will set the LLDP with interface_location, interface,
legacy_protocols, management_address, and snmp under the `vyos` top level key.  

### Implement using tasks

The `configure_lldp` function can also be implemented using the `tasks` directive
instead of the `roles` directive.  By using the `tasks` directive, you can
control when the fact collection is run. 

Below is an example of how to use the `configure_lldp` function with `tasks`.

```
- hosts: vyos

  tasks:
    - name: set lldp to vyos devices
      import_role:
        name: ansible-network.vyos
        tasks_from: configure_lldp
      vars:
        lldp:
          - interface_location: all
            interface: eth0
            legacy_protocols: cdp
            management_address: 192.168.1.1
            snmp: true
```

## Adding new parsers

Over time new parsers can be added (or updated) to the role to add additional
or enhanced functionality.  To add or update parsers perform the following
steps:

* Add (or update) command parser located in `parse_templates/cli`

## Arguments

### interface_location

To Set LLDP listening interfaces.

The default value is `omit` which means even if the user doesn't pass the respective
value the role will continue to run without any failure.

### interface

To Disable LLDP on respective interface.

The default value is `omit` which means even if the user doesn't pass the respective
value the role will continue to run without any failure.

### legacy_protocols

To Support other protocols over LLDP.

The default value is `omit` which means even if the user doesn't pass the respective 
value the role will continue to run without any failure.

### management_address

To define LLDP management-address.

The default value is `omit` which means even if the user doesn't pass the respective
value the role will continue to run without any failure.

### snmp

To enable SNMP queries of the LLDP database. Please note that SNMP must be already 
configured to enable LLDP SNMP.

The default value is `omit` which means even if the user doesn't pass the respective
value the role will continue to run without any failure.

### state

This sets the LLDP value to the VyOS device and if the value of the state is changed
to `absent`, the role will go ahead and try to delete the condifured LLDP via the arguments
passed.

The default value is `present` which means even if the user doesn't pass the respective
argument, the role will go ahead and try to set the LLDP via the arguments passed to the 
VyOS device.

## Notes

None
