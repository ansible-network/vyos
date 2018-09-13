# Configure VPN as responder
The `cloud_vpn/configure_vpn_responder` function will configure IPSEC VPN as responder
on VyOS devices.
It is performed by calling the `cloud_vpn/configure_vpn_responder` task from the role.
The task will process variables needed for VPN configuration and apply it to the device.

Below is an example to configure an IPSEC VPN as responder on VyOS device, where
the initiator is VyOS device:

```
- hosts: vyos

  tasks:
    - name: Configure IPSEC VPN as responder
      include_role:
        name: ansible-network.vyos
        tasks_from: cloud_vpn/configure_vpn_responder
      vars:
        cloud_vpn_name: myvpn
        cloud_vpn_psk: mypsksecret
        cloud_vpn_responder_provider: vyos
        cloud_vpn_responder_tunnel_ip: 169.254.56.26
        cloud_vpn_responder_outside_interface: eth0
        cloud_vpn_responder_private_ip: 10.0.0.10
        cloud_vpn_responder_tunnel_ip: 169.254.56.25
        cloud_vpn_initiator_provider: vyos
        cloud_vpn_initiator_public_ip: 18.191.132.220
```

## Notes
None
