# Lab Walkthrough and Documentation Checklist

Follow the official lab handout for the complete procedure. This document is a portfolio checklist, not a replacement for the lab's supplied VM scripts.

## Part 1 — Preparing the virtual environment
- [ ] Open the CyberOps Workstation VM in VirtualBox.
- [ ] Check the network adapter mode according to the handout (bridged, or NAT if required by your setup).
- [ ] In the VM, run the provided DHCP configuration script with the required privileges.
- [ ] Verify the VM has an IP address using the method in the handout.
- [ ] Test connectivity as directed and stop the ping with Ctrl+C.
- **Interface/IP observation:** TODO
- **Connectivity result:** TODO
- **Screenshot:** `screenshots/01-environment-connectivity.png`

The handout notes that if memory errors occur, the VM may need additional memory; it mentions trying 2 GB when the default 1 GB is insufficient.

## Part 2 — Firewall and IDS logs

### Step 1: Real-time IDS log monitoring
- [ ] Start the lab-provided Mininet topology script in the CyberOps VM.
- [ ] At the Mininet prompt, open an R1 shell.
- [ ] Start Snort using the supplied lab script and leave it running.
- [ ] Open shells for H5 and H10.
- [ ] Start the lab test web server on H10.
- [ ] Verify the listening service using the command in the handout.
- [ ] Open another R1 shell and follow the Snort alert log.
- [ ] From H5, perform the test transaction exactly as described in the lab.
- [ ] Record whether the transfer completed and whether an IDS alert appeared.
- **R1 shell user and prompt indicator:** TODO
- **Test server port observed:** TODO
- **Download result:** TODO
- **Alert generated and message:** TODO
- **Screenshot:** `screenshots/02-mininet-topology.png`
- **Screenshot:** `screenshots/03-snort-running.png`
- **Screenshot:** `screenshots/04-snort-alert.png`

### Record alert fields
Use your own Snort alert output:
- **Timestamp:** TODO
- **Signature/message:** TODO
- **Source IPv4 address:** TODO
- **Source port:** TODO
- **Destination IPv4 address:** TODO
- **Destination port:** TODO
- **Screenshot:** `screenshots/05-alert-fields.png`

### Packet capture
- [ ] Start `tcpdump` on the H5 interface specified by the handout, saving to the named PCAP file.
- [ ] Repeat the lab transaction inside the isolated lab environment.
- [ ] Stop the capture using the method described in the handout.
- [ ] Verify the PCAP exists and has a non-zero size.
- **PCAP filename:** TODO
- **Packet count from your output:** TODO
- **How PCAP can support analysis:** TODO
- **Screenshot:** `screenshots/06-packet-capture.png`

Do not publish the executable or raw capture unless your instructor explicitly authorizes it. A sanitized screenshot or short text summary is safer for a public portfolio.

### Step 2: Tune firewall rules based on IDS alerts
- [ ] Open a separate R1 shell.
- [ ] Inspect the current `iptables` rules.
- [ ] Identify the active chains shown in the output.
- [ ] Add the lab handout's specified TCP destination/port drop rule to the `FORWARD` chain, in the lab only.
- [ ] List rules again to confirm the rule appears.
- [ ] Repeat the test transaction from H5 and record the outcome.
- **Chains observed before the rule:** TODO
- **Rule appears in FORWARD output:** TODO
- **Connection/download outcome after rule:** TODO
- **Explanation based on evidence:** TODO
- **Alternative blocking approach discussed in the handout:** TODO
- **Screenshots:** `07-iptables-before.png`, `08-iptables-after.png`, `09-blocked-connection.png`

## Part 3 — Terminate and clear Mininet
- [ ] Exit Mininet with `quit` in the Mininet terminal.
- [ ] Run the cleanup command as described in the handout.
- **Cleanup result:** TODO
- **Screenshot:** `screenshots/10-cleanup.png`

## Final reflection
Write a few sentences on:
1. What you learned about IDS signature alerts.
2. How a PCAP can support a later investigation.
3. Why the `FORWARD` chain is relevant to transit traffic.
4. What evidence demonstrated the firewall rule's effect.
5. What you would investigate next.
