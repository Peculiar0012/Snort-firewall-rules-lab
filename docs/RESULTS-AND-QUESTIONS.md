# Results and Lab Questions

Complete this document using evidence from your own run. The source handout includes example output; do not copy its example timestamps, packet counts, or alert values as if they came from your session.

## Part 2, Step 1 — Real-Time IDS Log Monitoring

### 1. R1 shell
**Question:** What user is logged into the R1 shell? What is the indicator?  
**Your answer:** TODO

### 2. Test server connection
**Question:** What port is used when communicating with the test web server? What is the indicator?  
**Your answer:** TODO

### 3. Transfer and alert
**Question:** Was the file completely downloaded?  
**Your answer:** TODO

**Question:** Did the IDS generate any alerts related to the transaction?  
**Your answer:** TODO

### 4. Alert fields
**Source IPv4 address:** TODO  
**Destination IPv4 address:** TODO  
**Source port:** TODO  
**Destination port:** TODO  
**Timestamp:** TODO  
**IDS signature/message:** TODO

### 5. PCAP
**Question:** How can the PCAP file be useful to a security analyst?  
**Your answer:** TODO

## Part 2, Step 2 — Tuning Firewall Rules

### 6. Existing chains
**Question:** What chains are currently in use by R1?  
**Your answer:** TODO

### 7. Verify the block
**Question:** Was the download successful after the rule was added? Explain using your observed output.  
**Your answer:** TODO

### 8. Alternative blocking approach
**Question:** What would be a more aggressive but valid approach to blocking the offending server, according to the lab question?  
**Your answer:** TODO

## Part 3 — Cleanup
**Was Mininet terminated and cleaned up?** TODO

## Evidence summary
| Evidence item | Screenshot |
|---|---|
| VM connectivity | `screenshots/01-environment-connectivity.png` |
| Mininet topology | `screenshots/02-mininet-topology.png` |
| Snort running | `screenshots/03-snort-running.png` |
| Snort alert | `screenshots/04-snort-alert.png` |
| Alert fields | `screenshots/05-alert-fields.png` |
| Packet capture | `screenshots/06-packet-capture.png` |
| Rules before/after | `screenshots/07-iptables-before.png`, `screenshots/08-iptables-after.png` |
| Connection after block | `screenshots/09-blocked-connection.png` |
| Cleanup | `screenshots/10-cleanup.png` |
