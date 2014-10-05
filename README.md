getnets
=======

Description: get ISP inetnums by ASN or maintainer name with inverse lookup keys
--------------------------------------------------------------------------------

Usage:<br />
------------
getnets -m|--mount [mantainer name] -a|--as [ASN] -s|--server [server]<br />
getnets -h|--help for help<br />

Dependency:<br />
-----------------
**bash** 4.3.029<br />
**whois** 5.1.3<br />
**ipcalc** 0.41<br />
**grep** 2.20<br />
**awk** (gawk) 4.1.1<br />
**coreutils** 8.23<br />
Specified version is one that I use while write this script, I think it
can work on any version of this utilities (but may be not).<br/>

This little bash script help you found all ISP IPv4 networks (inetnums).
It can do so by search in RIR database for mnt-by and mnt-lower inverse 
lookup keys, if you know and provide mantainer name with -m parameter.<br />
**!NOTE:** blocks from mnt-lower can cross with mnt-by, but be a supernets
for latter.<br />
Another way to do so is to use authonomous system number (ASN) with -a
parameter.<br />
**!NOTE:** you can't specify both ASN and mantainer name.<br />
By default it use RIPE NCC database. If you specify server name with -s
you can query another RIR db, but be carefull as it use RIPE keys and
waiting for RIPE output.
