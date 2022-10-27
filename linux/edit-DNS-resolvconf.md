# Edit DNS Entries when managed by resolvconf

When DNS is managed my resolvconf (Recent versions of Raspbian for example) you cannot edit resolv.conf directly as it is managed by resolvconf.

To edit DNS:

1. Edit `/etc/dhcpcd.conf` and add the following to the bottom or edit an existing entry: `static domain_name_servers=8.8.8.8 8.8.4.4`
2. Restart dhcpcd: `sudo service dhcpcd restart`
