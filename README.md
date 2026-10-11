# Snort and Firewall Rules Lab

**Cybersecurity portfolio project | Snort IDS · iptables · tcpdump · Mininet**

This repository is a documentation workflow for the Cisco NetAcad lab **Lab - Snort and Firewall Rules**. It is designed to help you record your own practical steps, screenshots, observations, and answers, then publish them with Git Bash.

## Lab objectives
- Prepare the CyberOps Workstation VM and verify connectivity.
- Start the supplied Mininet topology and Snort IDS.
- Monitor Snort alerts while observing the lab's test HTTP transaction.
- Capture traffic with `tcpdump` and verify the PCAP file was created.
- Inspect `iptables` chains and add the lab's test blocking rule to `FORWARD`.
- Record the effect of the rule and clean up Mininet.

## Lab environment
- Oracle VirtualBox
- Cisco CyberOps Workstation VM
- Mininet topology supplied with the lab
- Snort IDS
- Linux `iptables`
- `tcpdump`

## Repository structure
```text
snort-firewall-rules-lab/
├── README.md
├── .gitignore
├── docs/
│   ├── LAB-WALKTHROUGH.md
│   ├── RESULTS-AND-QUESTIONS.md
│   ├── TROUBLESHOOTING.md
│   └── SCREENSHOT-PLAN.md
├── commands/
│   ├── README.md
│   └── command-reference.md
├── screenshots/
│   ├── README.md
│   └── .gitkeep
├── evidence/
│   ├── README.md
│   └── .gitkeep
└── scripts/
    └── README.md
```

## How to use
1. Read `docs/LAB-WALKTHROUGH.md` alongside your official lab handout.
2. Perform the lab only inside the provided/authorized virtual lab environment.
3. Save screenshots following `docs/SCREENSHOT-PLAN.md`.
4. Complete `docs/RESULTS-AND-QUESTIONS.md` with what you actually observed.
5. Use `commands/command-reference.md` as a reference, checking each command's context before running it.
6. Review `.gitignore`, then publish the folder using the Git Bash commands below.

## Push to GitHub with Git Bash
Create a new empty repository on GitHub first, for example `snort-firewall-rules-lab`. Do not initialize it with a README, license, or `.gitignore`.

From Git Bash opened inside the extracted project folder, run these commands one at a time. Replace `YOUR-USERNAME` with your GitHub username.

```bash
git init
git add .
git commit -m "Add Snort and firewall rules lab documentation"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/snort-firewall-rules-lab.git
git push -u origin main
```

If the remote already exists:
```bash
git remote set-url origin https://github.com/YOUR-USERNAME/snort-firewall-rules-lab.git
```

## Safety and portfolio quality
- Use only the supplied/authorized lab environment for the lab's malware-themed test transaction.
- Do not download or execute the sample on your everyday computer.
- Do not commit malware files, raw PCAPs, credentials, tokens, private keys, or sensitive logs.
- Use your own screenshots; do not present the handout's sample output as your own.
- Redact personal information and sensitive network details before publishing.
- This repository is a template: fill in all `TODO` items with your own observations.

## Source
Based on the user-provided Cisco Networking Academy handout, *Lab - Snort and Firewall Rules* (© 2018–2020). The lab VM scripts and sample executable are not included.
