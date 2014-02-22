fritz2graphite
==============

fritz2graphite is a command line tool written in shell to gather statistics from an upnp enabled FritzBox DSL router

fritz2graphite is based on upnp2mrtg, available at http://www.anetzb.de/upnp2mrtg/

Usage
-----
```
Usage: fritz2graphite [-a <host>] [-p <port>] [-G <port>] [-P <prefix>] [-d] [-h] [-i] [-t] [-v] [-V] -g <host>

  -a <host>    hostname or ip address of upnp device (default: fritz.box)
  -p <port>    port to connect (default: 49000)
  -g <host>    hostname or ip address of the graphite server
  -G <port>    carbon port on the graphite server (default: 2003)
  -P <prefix>  prefix for the graphite path (default: fritz_box)
  -d           debug mode
  -h           show help and exit
  -i <outfile> get all igd description
  -t           test connection
  -v           show fritz2graphite version and exit
  -V           be verbose for testing
```

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
* netcat 1.10 , no configuration is required. (Create configuration file /etc/fritz2graphite.cfg with NETCAT="nc_q" or NETCAT="nc", if you have problems. There are some patched netcat 1.10 around the world with -q Options, which i could'nt not find in the original sources.)
* The GNU netcat, create configuration file /etc/fritz2graphite.cfg with NETCAT="netcat".
* some other netcat, use -d Option to debug fritz2graphite and drop me a note.

