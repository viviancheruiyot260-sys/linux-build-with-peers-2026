Lab 14: Network Configuration — Commands and Uses

1. `ifconfig` — Displays network interfaces and IP addresses.
2. `ip addr show` — Displays network interfaces and IP addresses (modern alternative to ifconfig).
3. `route` — Displays the routing table.
4. `ip route show` — Displays network routes and the default gateway.
5. `grep 127.0.0.1 /etc/hosts` — Searches for the loopback address in the hosts file.
6. `ping -c 4 127.0.0.1` — Tests local network connectivity.
7. `ping -c 4 localhost` — Tests connectivity to localhost by hostname.
8. `cat /etc/resolv.conf` — Displays DNS resolver settings.
9. `dig localhost.localdomain` — Queries DNS for a hostname.
10. `dig cserver.example.com` — Looks up the IP address associated with a hostname.
11. `dig -x 192.168.1.2` — Performs a reverse DNS lookup.
12. `netstat --help` — Displays netstat help and available options.
13. `netstat -tl` — Displays listening TCP sockets.
14. `netstat -tln` — Displays listening TCP sockets with numeric addresses and ports.
15. `netstat -ltn` — Displays listening TCP sockets with numeric addresses and ports.
16. `ss` — Displays network socket connections and their states.
17. `ss -s` — Displays socket statistics.
18. `ss -ltn` — Displays listening TCP sockets with numeric addresses and ports.
19. `start_webserver` — Starts the lab web server and generates network traffic (training environment only).
20. `cat /etc/services` — Displays standard network service names and port numbers.

Modern Ubuntu alternatives:
- `ifconfig` → `ip addr show`
- `route` → `ip route show`
- `netstat` → `ss`
