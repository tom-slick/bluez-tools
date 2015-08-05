

# News #
Current release: **v0.1.38-662e** <br />
Changelog:
> - Fixed issues [#4](http://code.google.com/p/bluez-tools/issues/detail?id=4&can=1), [#5](http://code.google.com/p/bluez-tools/issues/detail?id=5&can=1), [#6](http://code.google.com/p/bluez-tools/issues/detail?id=6&can=1), [#7](http://code.google.com/p/bluez-tools/issues/detail?id=7&can=1) <br />

# About #
This is a GSoC'10 project to implement a new command line tools for [bluez](http://www.bluez.org/) (bluetooth stack for linux). The project implemented in C and uses the D-Bus interface of bluez. <br />
**Project Git repository**: http://gitorious.org/bluez-tools

# Features #
## bt-adapter ##
  * List available adapters
  * Show information about adapter (incl properties)
  * Discover remote devices (with remote device name resolving)
  * Change adapter properties (eg. Name, Discoverable, Pairable, etc)
## bt-agent ##
  * Manage incoming Bluetooth requests (eg. request of pincode, request of authorize a connection/service request, etc)
## bt-audio ##
  * Connecting to audio devices
## bt-device ##
  * List added devices
  * Connect to the remote device by his MAC, retrieve all SDP records and then initiate the pairing
  * Disconnect the remote device
  * Remove device (and also the pairing information)
  * Show information about device (incl properties)
  * Service discovery
  * Change device properties (eg. Name, Trusted, Blocked, etc)
## bt-input ##
  * Connecting to input devices
## bt-monitor ##
  * Capturing D-Bus signals of bluetoothd
## bt-network ##
  * Connect to the network device
  * Register network server for the provided UUID (gn/panu/nap)
## bt-serial ##
  * Connects to a specific RFCOMM based service on a remote device and then creates a RFCOMM TTY device for it
## bt-obex ##
  * Agent (to accept/reject incoming bluetooth object push requests) for OBEXD (OPP/FTP profile)
  * Send local file to the specified remote device using object push profile
  * Start FTP session with remote device

# Requirements #
bluez-tools requires at least **bluez-4.69** and **obexd-0.30**

# Known Issues #
  * FTP session closes unexpectedly after the command "ls" (**bug in OBEXD**?)
  * Copy/Move methods not yet implemented (OBEXD)