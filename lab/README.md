# SRv6 Deep Dive: lab files

The lab has six XRd vRouter nodes (PE1, P2, P3, P4, P5, PE6) and two Alpine Linux hosts (CE-A, CE-B).
The routers run IOS XR 26.2.2. The lab uses CML 2.10.0 or 2.10.1.

## Files

- `srv6-lab-v3.yaml`: the lab in the native CML format. Import it in CML with Import Lab. It lists the nodes, the links, and the start configuration of each node.
  The routers use the node definition `xrd-vr-e1000` and the image definition `xrd-vr-e1000-26-2-2`. This is a custom image in CML. Create it first, or change the names in the file to match yours. Each router uses 2 vCPU and 7168 MiB.
- `configs/<node>.cfg`: the running configuration of each router at the end of the experiments.
  This is the state after Episode 19. The port Gi0/0/0/4 on PE1 is the untrusted boundary port with the ACL SRV6-BOUNDARY-IN. The VPWS on PE1 is down in this state.
- `CE-addressing.md`: the interface addresses of the two CE hosts.

## Before you start

- The files have no real passwords. In the lab file, the password of the user cisco is CHANGE-ME. In the `.cfg` files, the password line is removed. Set your own password.
- The values of dynamic SIDs change after a reboot. Read them from the SID table. Do not copy them from the videos.
- The XR configuration stays after a node stop and start. A wipe returns the node to the start configuration in the lab file.

## License

Copyright 2026 Quintus Zhu. CC BY-NC-ND 4.0: https://creativecommons.org/licenses/by-nc-nd/4.0/
Third-party documents and trademarks belong to their owners.
