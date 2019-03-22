# NAPD
Nev's Anonymous Proxy Daemon

NAPD (nap d or napped) is a port-fowarding daemon that uses SSH tunnels to hide the IP address of the host.

For example, say you wanted to run a website from a server at your house, you would take a cheap virtual server and use NAPD to forward all traffic
via it. This would hide the IP address of your house while keeping a decently fast connection.

## Features

### Automatic setup

NAPD can be automatically deployed by simply running a script on the remote server and pasting its output into
the local server.

No need to copy SSH keys or create port forwarding rules on your firewall.

### Services running on other computers

As SSH tunnels allow the user to specify the IP address of the computer running the service,
this is also possible in NAPD.

For example, you have a Raspberry Pi running NAPD on the edge of your network and a test program running on your computer,
NAPD will be able to pass all traffic on an external port of a remote server directly to your RPI over the network

Of course, NAPD can also port-forward services running on the same computer as NAPD. 

### UPnP Support

> This feature is provisional and will probably be removed.

UPnP is a network protocol that allows devices on a network to request a port to be forwarded to the internet.

Sounds insecure, right? Yep. That's because it is.

UPnP on NAPD will allow devices to request ports and simply list them for manually validation later on either a web interface or CLI.

As a note, check your router/firewall and make sure UPnP is off.

### Web Interface

The plan is to add a web interface/API to NAPD for easy management. It's early days and this will take a while to implement.

### CLI

NAPD will come with a CLI for management rather than wasting hours of your life with config files. That's still an option if you're that way inclined.
