# Cisco-IOS-XE-and-IOS-XE-SD-WAN-Software
Cisco IOS XE is a single image that can be used to deploy both IOS XE and IOS XE SD-WAN on supported platforms.

This universalk9 image supports two modes: autonomous mode (for Cisco IOS XE features) and controller mode (for Cisco SD-WAN features) and it is available in release 17.2.x and later.

You access the Cisco IOS XE and Cisco IOS XE SD-WAN functionality through autonomous and controller execution modes, respectively. The autonomous mode is the default mode for the routers and includes the Cisco IOS XE functionality. To access the Cisco IOS XE SD-WAN functionality, switch to the controller mode.

Use the controller-mode command in the privileged EXEC mode to switch between the controller and autonomous modes.

The controller-mode disable command switches the device to the autonomous mode.
```
Device# controller-mode disable
```
The controller-mode enable command switches the device to the controller mode.
```
Device# controller-mode enable
```
When the device mode is switched from the autonomous mode to the controller mode, the startup configuration and the information in NVRAM (certificates) are erased. This action is the same as the write erase command.

When the device mode is switched from the controller to autonomous, all Yet Another Next Generation (YANG)-based configuration is preserved and it can be reused if you switch back to the controller mode.

When you switch to the controller mode from the autonomous mode and switch back to the autonomous mode, the Cisco IOS XE configuration is not restored because the startup configuration is empty. You need to manually restore the configuration from the backup.

When you switch to the autonomous mode from the controller mode and switch back to the controller mode, the original configuration in the controller mode is preserved.

For more information on the operational mode and the upgrade process, see https://www.cisco.com/c/en/us/td/docs/routers/sdwan/configuration/sdwan-xe-gs-book/install-upgrade-17-2-later.html.
