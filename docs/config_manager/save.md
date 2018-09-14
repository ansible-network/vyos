# Save active configuration to config.boot
The `save` function will save the current active configuration to
config.boot. This function is idempotent.

## How to save the active configuration
To save the current active configuration to config.boot simply
invoke the `save` function on the target device. There are no
additional configuration options available for this function.

Below is an example of calling the `save` function from the playbook.

```
- hosts: vyos

  roles:
    - name: ansible-network.vyos
      function: config_manager/save
```

## Arguments

None

## Notes
None
