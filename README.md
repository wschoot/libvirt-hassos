# HassOS in libvirt
This will install HassOS 5.10 in a virtual machine on your host using libvirt. It will create a default user (`admin` / `admin`). 

Tested on Ubuntu 20.10

## Requirements
- libvirt
- TI cc2531 USB dongle

## Usage
`ansible-playbook libvirt-hassos.yaml`

## Vars
See `vars.yml` for variables

```yaml
version: "5.10"
hassoshostname: hassos
```
# Configuration
## mqtt user
- `Configuration` -> `People`
  - Create user (my_user / my_password as default) for MQTT

## Advanced mode
- `Profile` -> `Advanced Mode`

# Add-ons
## Zigbee2mqtt
- `Supervisor` -> `Add-on Store` -> [...] -> `Repositories`
    - Add https://github.com/danielwelch/hassio-zigbee2mqtt

## Mosquitto Broker (mqtt)
-> `Supervisor` -> `Add-on Store` -> `Mosquitto broker` -> `Install`
> Note: By default, this broker uses system users

## Portainer (optional)
-> `Supervisor` -> `Add-on Store` -> `Portainer` -> `Install`
> Note: By default, system containers are hidden. Unhide with _Portainer_ -> _Settings_ -> _[Remove]_ (for each "Hidden container")
> Note: By default, _Protection mode_ is enabled. You might wanna disable this from time to time.

# Integration
## mqtt
Go to `integrations` and add the mqtt-integration
