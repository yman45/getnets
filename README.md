getnets
=======

Description: get ISP inetnums by ASN
-------------------------------------

Usage:<br />
------------
getnets ASN - where ASN is autonomous system number<br />
getnets -4 ASN or getnets --ipv4 ASN - same as first<br />
getnets -6 ASN or getnets --ipv6 ASN - for IPv6 subnets<br />
getnets -h|--help for help<br />

Dependency:<br />
-----------------
**bash** 4.3.042<br />
**whois** 5.2.7<br />
**sed** 4.2.2<br />
**coreutils** 8.24<br />
Specified version is one that I use while write this script, I think it
can work on any version of this utilities (but may be not).<br/>

This little bash script help you found all ISP IPv4 (or v6) networks (inetnums).
It can do so by search in RADB database and output one at a string.<br />
**NOTE** It can print network which can be sub(super)nets for already
printed network.
