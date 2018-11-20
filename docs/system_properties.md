# Configure System properties on the device

The `configure_sys_props` function can be used to set system properties on VyOS
devices.  This function is only supported over `network_cli` connection
type and requires the `ansible_network_os` value set to `vyos`.

## How to set System properties on the device

To set System properties on the device, simply include this function in the playbook
using either the `roles` directive or the `tasks` directive.  If no other
options are provided, then all of the available facts will be collected for the
device.

Below is an example of how to use the `roles` directive to set system properties
on the VyOS device.

```
- hosts: vyos

  roles:
  - name ansible-network.vyos
    function: configure_sys_props
  vars:
    system_properties:
      - hostname: test-vyos
        domain_name: hostname.com
        name_server: 192.168.1.1
```

The above playbook will set the hostname, domain-name and the name-server values to
the host under the `vyos` top level key.  

### Implement using tasks

The `configure_sys_props` function can also be implemented using the `tasks` directive
instead of the `roles` directive.  By using the `tasks` directive, you can
control when the fact collection is run. 

Below is an example of how to use the `configure_sys_props` function with `tasks`.

```
- hosts: vyos

  tasks:
    - name: set system properties to vyos devices
      import_role:
        name: ansible-network.vyos
        tasks_from: configure_sys_props
      vars:
        system_properties:
          - hostname: test-vyos
            domain_name: hostname.com
            name_server: 192.168.1.1
```

## Adding new parsers

Over time new parsers can be added (or updated) to the role to add additional
or enhanced functionality.  To add or update parsers perform the following
steps:

* Add (or update) command parser located ino `parse_templates/cli`

## Arguments

### hostname

This will set the System host name for the VyOS device.

The default value is `omit` which means even if the user doesn't pass the respective
value the role will continue to run without any failure.

### domain_name

This will set the System domain name for the VyOS device.

The default value is `omit` which means even if the user doesn't pass the respective 
value the role will continue to run without any failure.

### name_server

This will set the Domain Name Server (DNS) for the VyOS device.

The default value is `omit` which means even if the user doesn't pass the respective 
value the role will continue to run without any failure.

### state

This will set the hostname, domain-name and name-server value to the VyOS device and if
the value of the state is changed to `absent`, role will go ahead and try to delete the
hostname, domain-name and name-server passed via the arguments.

The default value is `present` which means even if the user doesn't pass the respective
argument, role will go ahead and try to set the hostname, domain-name and name-server 
via the arguments passed to the VyOS device.

## Notes

None
