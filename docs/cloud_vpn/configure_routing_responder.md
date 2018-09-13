# Configure VPN routing as responder
The `cloud_vpn/configure_routing_responder` function will configure the routing where
a VPN as responder has been configured previously on VyOS devices.
It is performed by calling the `cloud_vpn/configure_routing_responder` task from the role.
The task will process variables needed for routing configuration and apply it to the device.

Below is an example to configure routing on a VyOS device configured as responder,
where the responder is VyOS.

```
- hosts: vyos

  tasks:
    - name: Configure responder routing
      include_role:
        name: ansible-network.vyos
        tasks_from: cloud_vpn/configure_routing_responder
      vars:
        cloud_vpn_initiator_provider: vyos
        cloud_vpn_initiator_cidr: 10.0.0.0/24
```

## Notes
None
