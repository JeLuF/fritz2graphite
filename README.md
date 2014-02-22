fritz2graphite
==============

fritz2graphite is a command line tool written in shell to gather statistics from an upnp enabled FritzBox DSL router

fritz2graphite is based on upnp2mrtg, available at http://www.anetzb.de/upnp2mrtg/

netcat
------

There are different incarnations of netcat. Type

    nc -h

to check which on you use:
* The GNU Netcat http://sourceforge.net/projects/netcat (Version 0.7.1 , 2004-01-10)
* OpenBSD netcat http://www.openbsd.org/cgi-bin/cvsweb/src/usr.bin/nc/ (Version 1.97, 2010-05-19)
* netcat 1.10 http://www.unknown-site/netcat/ (Version 1.10 , 1996-03-20)
* ... or some other ...

Configuration
-------------

If you use ...
* netcat 1.10 , no configuration is required. (Create configuration file /etc/upnp2mrtg.cfg with NETCAT="nc_q" or NETCAT="nc", if you have problems. There are some patched netcat 1.10 around the world with -q Options, which i could'nt not find in the original sources.)
* The GNU netcat, create configuration file /etc/upnp2mrtg.cfg with NETCAT="netcat".
* some other netcat, use -d Option to debug upnp2mrtg and drop me a note.

