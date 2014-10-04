getnets
=======

get isp networks by as or mnt-* attributes

Usage:
getnets -m|--mount [mnt-* attribute] -a|--as [ASN] -s|--server [server]
getnets -h or --help for help

This little bash utility help you found all ISP networks.
It can do so by search in database for mnt-by and mnt-lower entries
if you know and provide mounter name with -m parameter.
!NOTE: blocks from mnt-lower can cross with mnt-by, but be a supernets
for latter.
Another way to do so is to use authonomous system number (ASN) with -a
parameter.
!NOTE: you can't specify both ASN and mnt-* attrubute.
By default it use RIPE NCC database. If you specify server name with -s
you can query another db, but be carefull as it use RIPE attributes and
wait for RIPE output.
