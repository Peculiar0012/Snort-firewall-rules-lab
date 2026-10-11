# Command Reference — Snort and Firewall Rules

| Purpose | Command from/associated with the handout | Run context |
|---|---|---|
| Configure DHCP | `sudo ./lab.support.files/scripts/configure_as_dhcp.sh` | CyberOps Workstation VM |
| Check interface/IP | `ifconfig` | CyberOps Workstation VM |
| Test connectivity | `ping www.cisco.com` | CyberOps Workstation VM; stop with Ctrl+C |
| Start Mininet topology | `sudo ./lab.support.files/scripts/cyberops_extended_topo_no_fw.py` | CyberOps Workstation VM |
| Open R1 terminal | `xterm R1` | Mininet prompt |
| Start Snort | `./lab.support.files/scripts/start_snort.sh` | R1 shell, as directed by handout |
| Monitor alert log | `tail -f /var/log/snort/alert` | Separate R1 shell |
| Start lab test server | `./lab.support.files/scripts/mal_server_start.sh` | H10 shell, lab only |
| Check listening services | `netstat -tunpa` | H10 shell |
| Capture packets | `tcpdump -i H5-eth0 -w nimda.download.pcap &` | H5 shell, lab only |
| Bring capture forward | `fg`, then Ctrl+C | H5 shell |
| Verify capture file | `ls -l` | H5 shell |
| List firewall rules | `iptables -L -v` | R1 shell |
| Lab-specific blocking rule | `iptables -I FORWARD -p tcp -d 209.165.202.133 --dport 6666 -j DROP` | R1 shell in the supplied isolated topology only |
| Exit Mininet | `quit` | Mininet prompt |
| Clean up Mininet | `sudo mn -c` | CyberOps Workstation VM |

## Important
- IP addresses, interface names, script paths, and the test port are specific to this handout's lab topology.
- The lab-specific blocking rule is documentation for the supplied exercise, not a general blocklist recommendation.
- Do not fetch or run the malware-themed sample on your everyday computer.
- This repository intentionally does not include the supplied VM scripts, malware sample, or raw packet captures.
