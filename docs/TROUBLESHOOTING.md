# Troubleshooting Notes

Record the issue, the context, what you checked, and the outcome. Follow the course handout and instructor guidance.

| Symptom | Checks to document |
|---|---|
| VM has no network address | Confirm the VM adapter mode and whether the provided DHCP configuration script completed. |
| Ping/connectivity check fails | Record the exact error, confirm network setup, and note whether the course network requires a different adapter mode. |
| Mininet does not reach its prompt | Record startup errors and confirm the correct lab VM and supplied topology script are being used. |
| Snort stops or exits | The handout says Snort must remain running for later alert capture; record the output and follow the lab's restart guidance. |
| No alert appears | Confirm the alert log is being monitored in the correct R1 shell and record what actually happened. Do not assume an alert occurred. |
| PCAP is missing or empty | Verify the capture was started on the intended H5 interface, the transaction occurred during capture, and capture was stopped as instructed. |
| Firewall result differs from expectation | Capture rule output before and after, record the connection result, and check that commands were run in the correct R1 shell. |
| Memory error | The handout notes increasing VM memory; it mentions trying 2 GB if the default 1 GB is insufficient. |

## My troubleshooting log
- **Date/time:** TODO
- **Symptom/error:** TODO
- **Checks performed:** TODO
- **Resolution/outcome:** TODO
- **Evidence file:** TODO
