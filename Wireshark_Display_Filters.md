# Wireshark - Simple Display Filters

Here you'll find basic display filters (and a few more specific) to use in Wireshark.</br>
Detailled information here: <https://www.wireshark.org/docs/man-pages/wireshark-filter.html>

## OR condition

    arp or dns

    http || tls

## AND condition

    http && ip.src == 10.0.0.1

## source/destination address

    eth.src == ff:ff:ff:ff:ff:ff

    eth.src == ff-ff-ff-ff-ff-ff

    eth.dst == ffff.ffff.ffff

## ip address

    ip.addr == 10.0.0.1

    !(ip.addr == 10.0.0.1)

## ip address range

    ip.addr == 10.0.0.0/24

## source/destination ip

    ip.src == 10.0.0.1

    ip.dst == 10.0.0.1

    ip.dst != 10.0.0.1

    ip.src != 10.0.0.1

## port number

    tcp.port eq 80

    tcp.port == 443

    udp.port == 53

    tcp.dstport == 3389

    udp.srcport == 50000

## protocol

    http

    dns

    arp

    !(arp or icmp or dns)

## http method

    http.request.method == GET or http.request.method == POST and ip.host == 10.0.0.1

    http.request.uri == "https://www.wireshark.org/"

    http.response.code == 200

## https to specific ip

    tcp.port == 443 and ip.addr == 1.2.3.4

## specific protocol, specific ip

    (http or ftp) and ip.addr == 192.168.1.14

## conversation

    (ip.src == 10.0.0.1 and ip.dst == 10.0.0.2) or (ip.src == 10.0.0.2 and ip.dst == 10.0.0.1)

## ssl handshake - client hello/server hello

    ssl.handshake.type == 1

    ssl.handshake.type == 2

## dhcp only related

    udp.dstport == 67 || udp.dstport == 68
