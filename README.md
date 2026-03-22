# Mikrotik
Catatan mikrotik lunacomp

# STATIC ROUTING GAMES USING FILTER RAW
```
#########################################################
# Static Routing Games Using Filter Raw Generator - Buananet.com
# Date/Time: 3/22/2026, 10:48:28 PM
# Created By: buananet.com - fb.me/buananet.pbun
#########################################################
/ip firewall address-list
add list=LOCAL-IP address=10.0.0.0/8 comment="Routing Games by buananet.com"
add list=LOCAL-IP address=172.16.0.0/12 comment="Routing Games by buananet.com"
add list=LOCAL-IP address=192.168.0.0/16 comment="Routing Games by buananet.com"
/ip route
add gateway=192.168.18.1 routing-mark=routing-game comment="Routing Games by buananet.com"
/ip firewall mangle
add action=mark-routing chain=prerouting connection-mark=conn-game new-routing-mark=routing-game passthrough=no src-address-list=LOCAL-IP comment="Routing Games by buananet.com" place-before=*0
add action=mark-connection chain=prerouting dst-address-list=List-IP-Games new-connection-mark=conn-game passthrough=yes comment="Routing Games by buananet.com" place-before=*0
##############################################################
# If you want to add a game script only, you can ignore the script above
##############################################################
/ip firewall raw
# Clash Of Clans - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Clash Of Clans - Mobile" dst-address-list=!LOCAL-IP dst-port=9330-9340 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=9330-9340 protocol=udp
# Clash Royale (Cry) - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Clash Royale (Cry) - Mobile" dst-address-list=!LOCAL-IP dst-port=9330-9340 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=9330-9340 protocol=udp
# Call Of Duty - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Call Of Duty - Mobile" dst-address-list=!LOCAL-IP dst-port=3013,10000-10019,18082,50000,65010,65050 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=7085-7995,8700,9030,10010-10019,17000-20100 protocol=udp
# DOTA2 - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="DOTA2 - Mobile" dst-address-list=!LOCAL-IP dst-port=9100-9200,8230-8250,8110-8120,27000-28998 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=27000-28998,39000 protocol=udp
# FIFA ONLINE - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="FIFA ONLINE - Mobile" dst-address-list=!LOCAL-IP dst-port=7770-7790 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=16300-16350 protocol=udp
# Free Fire - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Free Fire - Mobile" dst-address-list=!LOCAL-IP dst-port=6006,6674,7006,7889,8001-8012,9006,9137,10000-10012,11000-11019 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=12006,12008,13006,15006,20561,39003,39006,39698,39779,39800 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=6006,6008,7008,8008,8130,8443,9008,9120,10000-10015,10100,11000-11019,12008,13008 protocol=udp
# Minecraft - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Minecraft - Mobile" dst-address-list=!LOCAL-IP dst-port=25565,19132-19133 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=25565,19132-19133 protocol=udp
# Mobile Legends - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Mobile Legends - Mobile" dst-address-list=!LOCAL-IP dst-port=5000-5221,5224-5227,5229-5241,5243-5508,5551-5559,5601-5700,9000-9010,9443 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=5520-5529,10003,30000-30300,8443 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=4001-4009,5000-5221,5224-5241,5243-5509,5551-5559,5601-5700,8130,8443,9120 protocol=udp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=2702,3702,5517,5520-5529,8001,9000-9010,9992,10003,30000-30300 protocol=udp
# Point Blank - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=44590-44610 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Point Blank - Mobile" dst-address-list=!LOCAL-IP dst-port=40000-40010 protocol=udp
# PUBG - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="PUBG - Mobile" dst-address-list=!LOCAL-IP dst-port=7889,10012,13004,14000,17000,17500,18081,20000-20002,20371 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=8011,9030,10491,10612,12235,13004,13748,17000,17500,20000-20002 protocol=udp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=7086-7995,10039,10096,11455,12070-12460,13894,13972,41182-41192 protocol=udp
# Roblox - Mobile
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting comment="Roblox - Mobile" dst-address-list=!LOCAL-IP dst-port=3074 protocol=tcp
add action=add-dst-to-address-list address-list="List-IP-Games" address-list-timeout=1d chain=prerouting dst-address-list=!LOCAL-IP dst-port=88,500,3074,3544,4500,49152-65535 protocol=udp
```
