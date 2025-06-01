# SKYNET Blocklist

SKYNET is a firewall developed by Adamm00. The project is available at:

https://github.com/Adamm00/IPSet_ASUS

This repository is dedicated to the development, testing, and sharing of improved blocklists and settings for SKYNET. This malware IP blocklist is designed to enhance network security by blocking inbound and outbound connections to known malicious hosts, with a strong emphasis on outbound control to disrupt command-and-control (C2) traffic.

## Purpose

This project provides a comprehensive IP blocklist to:

- Block traffic from state sponsors of terrorism
- Enforce compliance with OFAC and international sanctions
- Prevent data exfiltration and reconnaissance from hostile foreign actors
- Mitigate risks from nation-state surveillance, cyberattacks, and abuse

It is intended for network administrators, security engineers, and defenders who want to proactively reduce their exposure surface to geopolitical cyber threats.

## Data Sources

This blocklist is compiled from multiple authoritative sources including:

### Sanctioned and Watchlisted Countries

- Blockpass – Sanctions List Countries
- USCIRF 2025 Recommendations
- U.S. Department of State – Countries of Particular Concern
- U.S. Department of Energy – Countries of Risk
- OFAC & State Sponsors of Terrorism Lists

### Threat Intelligence Feeds

- FireHOL IP Threat Lists:
  - Malware command-and-control IPs
  - Spam, proxy, TOR, anonymous VPN endpoints
  - Botnets, scanners, compromised devices
  - High-risk country-based IP blocks (IPv4 and IPv6)

## What's Included

- IP addresses and CIDR blocks for:
  - High-risk countries (e.g., China, Russia, Iran, North Korea)
  - Surveillance and censorship-heavy regimes
  - OFAC sanctioned entities and threat actors
  - Open proxies, anonymizers, TOR exit nodes
  - Malware-infected hosts and botnets

## Disclaimer

> Use this blocklist responsibly. Blocking entire countries or IP ranges may impact legitimate services and users. This list is provided as-is for defensive and compliance purposes. Always validate in a staging environment before production deployment.

## How to Use

### Step 1: Update the Blocklist

1. Launch the SKYNET interface.
2. Choose Option 3 ("Malware Blacklist").
3. Choose Option 2 ("Change filter list").
4. Enter the following blocklist URL:

```
https://raw.githubusercontent.com/collingeorge/SKYNET/refs/heads/main/blocklist
```

### Step 2: Disable CDN Whitelisting

To improve effectiveness and prevent malware and command and control network bypasses:

1. In the SKYNET main menu, choose Option 11 (Settings).
2. Choose Option 14 ("CDN Whitelisting").
3. Choose Option 2 ("Disable").

### What to Expect

- Allow SKYNET to run for at least 24 hours.
- After this period, log in and check block statistics.
- You should begin to see both inbound and outbound IPs being blocked.

> Outbound blocks are especially valuable, as they can stop malware from connecting to external control servers (C2 infrastructure).

## Credits

This blocklist integrates and builds upon the work by the FireHOL IP Lists Project, as well as additional threat intelligence from:

- HotCakeX's Official IANA IP Blocks
- ThreatView
- Emerging Threats
- Crazy-Max's WindowsSpyBlocker
- HerrBischoff Country IP Blocks

## License

This repository follows the original licensing of the included blocklists. Please refer to the source project (FireHOL) for attribution and usage rights.

## Contribute

Have a trustworthy threat feed to recommend? Submit a pull request or open an issue.
