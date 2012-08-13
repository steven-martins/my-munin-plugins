my-munin-plugins
================

Some plugins for munin :

- fd_tomcat is a simple plugin which count the number of file descriptor currently used by tomcat and/or java.

- if_ : I decided to modify the original plugin to improve the visibility. Now, the plugin renders graphs which looks like to MRTG's graph (overlapped sent and received lines)

Examples are available in the directory "examples".


INSTALL
========

Plugins must be copied inside : /opt/munin/lib/plugins (The path is dependent of your installation)

if_:

To finish, if not already done; To monitor an interface, you need to create symbolic link with the plugin like :
ln -s /opt/munin/lib/plugins/if_ /etc/opt/munin/plugins/if_eth0
ln -s /opt/munin/lib/plugins/if_ /etc/opt/munin/plugins/if_lo

fd_tomcat:

The plugin need to run as root.  This is configured like this:

[fd_tomcat]
	user root

(This two lines should be pasted into a file (named like "fd_tomcat") inside the "plugin-conf.d" directory (e.g. /etc/opt/munin/plugin-conf.d)
