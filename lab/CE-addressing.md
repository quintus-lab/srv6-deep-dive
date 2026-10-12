# CE hosts: interface addresses

The two CE hosts run Alpine Linux. A reboot removes the addresses. Set them again.
eth0 is BLUE. eth1 is RED. eth2 is the boundary and VPWS test port.

## CE-A

- `eth0` 10.1.1.2/24
- `eth0` 2001:db8:c:101::2/64
- `eth1` 10.2.1.2/24
- `eth1` 2001:db8:c:201::2/64
- `eth2` 172.16.30.1/24
- `eth2` 2001:db8:ffff:1::2/64
- `eth2` 2001:db8:30::1/64

## CE-B

- `eth0` 10.1.6.2/24
- `eth0` 2001:db8:c:106::2/64
- `eth1` 10.2.6.2/24
- `eth1` 2001:db8:c:206::2/64
- `eth2` 172.16.30.6/24
- `eth2` 2001:db8:30::6/64

