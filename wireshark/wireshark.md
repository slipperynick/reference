# Wireshark Display Filter Reference

## Ethernet (Layer 2)
- **`eth.addr`**: Matches packets with the specified MAC address as either source or destination.
  - Example: `eth.addr == 00:1a:6b:ce:fc:bb`
- **`eth.src`**: Matches packets with the specified source MAC address.
  - Example: `eth.src == 00:1a:6b:ce:fc:bb`
- **`eth.dst`**: Matches packets with the specified destination MAC address.
  - Example: `eth.dst == 00:1a:6b:ce:fc:bb`

## ARP (Address Resolution Protocol)
- **`arp.dst.hw_mac`**: Matches packets with the specified target MAC address.
  - Example: `arp.dst.hw_mac == 00:1a:6b:ce:fc:bb`
- **`arp.dst.proto_ipv4`**: Matches packets with the specified target IPv4 address.
  - Example: `arp.dst.proto_ipv4 == 10.10.10.10`
- **`arp.src.hw_mac`**: Matches packets with the specified sender MAC address.
  - Example: `arp.src.hw_mac == 00:1a:6b:ce:fc:bb`
- **`arp.src.proto_ipv4`**: Matches packets with the specified sender IPv4 address.
  - Example: `arp.src.proto_ipv4 == 10.10.10.10`

## VLAN (Virtual Local Area Network)
- **`vlan.id`**: Matches packets with the specified VLAN ID.
  - Example: `vlan.id == 16`

## IPv4 (Internet Protocol Version 4)
- **`ip.addr`**: Matches packets with the specified IPv4 address as either source or destination.
  - Example: `ip.addr == 10.10.10.10`
- **`ip.src`**: Matches packets with the specified source IPv4 address.
  - Example: `ip.src == 10.10.10.10`
- **`ip.dst`**: Matches packets with the specified destination IPv4 address.
  - Example: `ip.dst == 10.10.10.10`
- **`ip.proto`**: Matches packets with the specified IP protocol number.
  - Example: `ip.proto == 1` (ICMP)

## IPv6 (Internet Protocol Version 6)
- **`ipv6.addr`**: Matches packets with the specified IPv6 address as either source or destination.
  - Example: `ipv6.addr == 2001::5`
- **`ipv6.src`**: Matches packets with the specified source IPv6 address.
  - Example: `ipv6.src == 2001::5`
- **`ipv6.dst`**: Matches packets with the specified destination IPv6 address.
  - Example: `ipv6.dst == 2001::5`

## TCP (Transmission Control Protocol)
- **`tcp.port`**: Matches packets with the specified TCP port as either source or destination.
  - Example: `tcp.port == 80`
- **`tcp.srcport`**: Matches packets with the specified source TCP port.
  - Example: `tcp.srcport == 60234`
- **`tcp.dstport`**: Matches packets with the specified destination TCP port.
  - Example: `tcp.dstport == 80`

## UDP (User Datagram Protocol)
- **`udp.port`**: Matches packets with the specified UDP port as either source or destination.
  - Example: `udp.port == 513`
- **`udp.srcport`**: Matches packets with the specified source UDP port.
  - Example: `udp.srcport == 40000`
- **`udp.dstport`**: Matches packets with the specified destination UDP port.
  - Example: `udp.dstport == 513`

## ICMP (Internet Control Message Protocol)
- **`icmp.type`**: Matches packets with the specified ICMP type code.
  - Example: `icmp.type == 8` (Echo request)

## Wireless LAN (IEEE 802.11)
- **`wlan.addr`**: Matches packets with the specified MAC address as either source or destination in wireless frames.
  - Example: `wlan.addr == 00:1a:6b:ce:fc:bb`
- **`wlan.sa`**: Matches packets with the specified source MAC address in wireless frames.
  - Example: `wlan.sa == 00:1a:6b:ce:fc:bb`
- **`wlan.da`**: Matches packets with the specified destination MAC address in wireless frames.
  - Example: `wlan.da == 00:1a:6b:ce:fc:bb`

## Routing Protocols
- **`bgp.originator_id`**: Matches packets with the specified BGP originator ID.
  - Example: `bgp.originator_id == 192.168.10.15`
- **`bgp.next_hop`**: Matches packets with the specified BGP next hop address.
  - Example: `bgp.next_hop == 192.168.10.15`
- **`rip.ip`**: Matches packets with the specified RIP IPv4 address.
  - Example: 
