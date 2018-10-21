# mIRC-server.ini
The version of server.ini supplied with mIRC is OK, but is inconsistent in terms of Random vs. individual servers,
and inaccurate on the ports supported.

This repo is a way to crowd-source a more consistent and accurate version of server.ini.

The rules for this version of server.ini are as follows:

1. Only Networks with a substantial user base should be included. For less popular networks, the user can add their own definitions.

1. Each Network should have a single Group of the same name as the Network.

1. In order that users have the best chance of connecting, wherever possible Random server addresses should be used 
i.e. DNS domain names which resolve to multiple IP addresses. 
DNS domain names which resolve to single IP addresses should only be used for networks which have a single IRC server.

1. Ports should be the lowest common denominator of ports for all servers mapped by the address 
(so that mIRC has the greatest chance of connecting on a first attempt).

1. SSL / TLS ports should be listed first so that mIRC will connect to them in preference.

1. New servers should be added to the end of the list rather than trying to insert them to maintain a consistent sort order.
(This is to avoid needing to change the `nxxx` sequence at the start of every line which would create commits with large number
of trivial "changes".)
The admins of this repo will occassionally sort the sequence as a separate commit.

Users will be able to download this server.ini to replace the standard one.
If we are lucky Khaled may agree to include it in mIRC itself rather than try to maintain a version himself.
**Note:** At the time of writing (Oct 2018) [the servers.ini available on the mIRC website](https://www.mirc.co.uk/servers.ini)
had not been updated since April 2016.
