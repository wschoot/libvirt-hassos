# HassOS in libvirt
## Requirements
- libvirt

### Zigbee2mqtt
- Supervisor -> Add-on Store -> [...] -> Repositories
    - Add https://github.com/danielwelch/hassio-zigbee2mqtt
### Advanced mode
- Enable Profile -> Advanced Mode

### mqtt
-> Supervisor -> Add-on Store -> Mosquitto broker -> Install
> Note: By default, this broker uses system users

### mqtt user
- Configuration -> People
  - Create user (my_user / my_password as default) for MQTT

### portainer (optional)
-> Supervisor -> Add-on Store -> Portainer -> Install
> Note: By default, system containers are hidden. Unhide with _Portainer_ -> _Settings_ -> _[Remove]_ (for each "Hidden container")