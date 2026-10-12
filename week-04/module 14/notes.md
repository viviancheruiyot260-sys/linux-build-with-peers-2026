Network Configuration

Linux provides tools to configure, inspect, and troubleshoot network connections, IP addresses, DNS, routing, and remote access.

## Key Networking Terms
- **IP address:** Identifies a device on a network.
- **IPv4:** Uses 32-bit addresses, e.g. `192.168.1.10`.
- **IPv6:** Uses 128-bit addresses.
- **DNS:** Translates domain names into IP addresses.
- **DHCP:** Automatically assigns network settings.
- **Gateway/router:** Forwards traffic between networks.
- **Packet:** A small unit of data sent across a network.
- **Hostname:** A human-readable name for a device.
- **TCP/IP:** Protocols used for network communication.

## Network Configuration
Network interfaces can use wired Ethernet or wireless Wi-Fi. IP settings can be assigned automatically through DHCP or manually using a static IP address.

Modern Ubuntu commonly uses Netplan configuration files in `/etc/netplan/`. Older CentOS examples may use `/etc/sysconfig/network-scripts/`; these paths are distribution-specific.

Important configuration files:
- `/etc/hosts` — local hostname-to-IP mappings.
- `/etc/resolv.conf` — DNS resolver configuration.
- `/etc/nsswitch.conf` — controls the order of name lookups.

## Network Commands

| Command | Purpose |
|---|---|
| `ip addr show` | Displays interfaces and IP addresses. |
| `ip link show` | Displays network interface status. |
| `ip route show` | Displays routing information. |
| `ip -s link` | Displays interface traffic statistics. |
| `ping -c 4 HOST` | Tests connectivity with four packets. |
| `host DOMAIN` | Looks up DNS information. |
| `ss -s` | Summarizes socket statistics. |
| `ss -tln` | Displays listening TCP sockets. |
| `ssh USER@HOST` | Connects securely to a remote computer. |
| `ssh-keygen -R HOST` | Removes a saved SSH host key after its change has been verified as legitimate. |

Older commands include `ifconfig`, `route`, and `netstat`. Modern alternatives are generally `ip`, `ip route`, and `ss`.

## Important Lessons
- A failed ping does not always mean a device is offline; firewalls may block ping requests.
- A port in the listening state does not guarantee that remote connections are allowed.
- If a domain lookup fails but an IP address works, DNS may be the problem.
- Verify unexpected SSH host-key changes before reconnecting.
- Inspect network settings carefully before making changes.

