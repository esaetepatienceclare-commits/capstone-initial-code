# Firewall Rule Loader – Week 2

## Files
- `rule_loader.c` – Loads firewall rules from a text file.
- `rules.txt` – Sample rule file.

## Rule Format
`<src_ip/mask> <dst_ip/mask> <src_port> <dst_port> <protocol> <action>`

- IP/mask: CIDR notation (e.g., `192.168.1.0/24`)
- Port: single number or range (e.g., `1024-65535`)
- Protocol: `tcp`, `udp`, `icmp`, `any`
- Action: `allow` or `deny`
- `#` at line start indicates a comment.

## Compile & Run for windows with MinGW
gcc -o rule_loader rule_loader.c -lws2_32
.\rule_loader.exe rules.txt
