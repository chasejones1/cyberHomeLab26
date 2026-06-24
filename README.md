# Cybersecurity Home Lab

A personal cybersecurity home lab built to develop hands-on skills in 
network security, intrusion detection, and offensive/defensive security techniques.

#Lab Environment

| Component | Details |
|-----------|---------|
| Host OS | Windows 11 |
| Hypervisor | Oracle VirtualBox 7.2 |
| Attacker VM | Kali Linux (192.168.110.102) |
| Defender VM | Ubuntu Server 24.04 (192.168.110.101) |
| Network | Host-Only isolated lab network |

## Security Stack Deployed

| Tool | Purpose | Status |
|------|---------|--------|
| Wazuh Manager | SIEM - Log collection and analysis | ✅ Active |
| Wazuh Agent | Endpoint monitoring on Kali and Ubuntu | ✅ Active |
| Suricata IDS | Network intrusion detection | ✅ Active |
| Fail2ban | Automated IP blocking | ✅ Active |

## Attacks Performed & Detected

### 1. Nmap SYN Stealth Scan
- **Tool:** Nmap
- **Command:** `sudo nmap -sS -A 192.168.110.101`
- **Purpose:** Network reconnaissance and port scanning
- **Detected by:** Suricata IDS
- **Result:** SSH service fingerprinted on port 22

### 2. SSH Brute Force Attack
- **Tool:** Hydra
- **Command:** `sudo hydra -l chasetgt -P wordlist.txt -t 4 192.168.110.101 ssh`
- **Purpose:** Password brute force against SSH
- **Detected by:** Fail2ban
- **Result:** Attacking IP automatically banned after 3 failed attempts

## Key Skills Demonstrated

- Virtual machine deployment and network configuration
- Linux server administration (Ubuntu Server)
- SIEM deployment and configuration (Wazuh)
- Network intrusion detection system setup (Suricata)
- Offensive security tools (Nmap, Hydra, Metasploit)
- Log analysis and alert triage
- Automated threat response (Fail2ban)
- LVM partition management
- SSL certificate generation and deployment

## Tools & Technologies

`Kali Linux` `Ubuntu Server` `VirtualBox` `Wazuh` `Suricata` `Fail2ban` 
`Nmap` `Hydra` `OpenSSH` `systemctl` `Linux CLI`

## Lab Network Diagram
