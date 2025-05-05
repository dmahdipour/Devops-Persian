Ban and control unauthorized access.
We have to configure builtin firewall addition to Hardware and Software firewalls.
Filtering IP address, IP range, port, etc.

### Iptables
A strong firewall that humanize the roles of IP by table and chains.
* Input chain      -> the ports that others have to access them, ex. 80, 443, 22
* Output chain   -> what can out from our servers (Open any access: who comes to server know how to manipulate iptables)
* Forward chain -> to another networks

We have two kind of list of IP access:
* *Whitelist*
* *Blacklist*

Two methods are using in this content for port policies:
* *All ports are open* (No secure)
* *All ports are ban* (Manage the ports that are necessary to be accessible.)

**Note:** Be careful about ports that are added to Iptables. ex: If change the ssh port but forgot to add new port to Iptable, you could not access to your server any more.

To have better performance we add roles to configuration files then address it to the firewall to update roles based on those files. In this case you can update and improve your roles day to day.

* iptables -save
* iptables -restore