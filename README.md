
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

- [Blockpass – Sanctions List Countries](https://help.blockpass.org/hc/en-us/articles/11881237145241-Which-countries-should-I-block-Sanctions-list-countries)
- [USCIRF 2025 Recommendations](https://www.uscirf.gov/countries/2025-recommendations)
- [U.S. Department of State – Countries of Particular Concern](https://www.state.gov/countries-of-particular-concern-special-watch-list-countries-entities-of-particular-concern/)
- [U.S. Department of Energy – Countries of Risk](https://www.energy.gov/science/countries-risk)

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

## Why This List is Better and What Changed

This updated blocklist is the result of **rigorous statistical analysis** performed on multiple IP blocklists to optimize coverage while minimizing overlap and redundancy. Key improvements include:

- **Maximized Unique IP Coverage:** By analyzing overlap among popular blocklists (primarily FireHOL’s), this list includes IP sets that cover the greatest number of malicious and suspicious addresses without duplicating entries. This leads to more efficient blocking and better use of firewall resources.

- **Reduced False Positives and Noise:** Overlapping blocklists often cause redundant blocking that may include benign IPs flagged multiple times. By carefully selecting non-overlapping sets, this list reduces potential false positives and unintended service disruptions.

- **Layered Defense Strategy:** The list combines core threat intelligence with specialized feeds such as SSH brute force attackers, proxy and anonymizer IPs, and country-specific high-risk blocks, providing a comprehensive multi-layered security posture.

- **Focused Geographic Filtering:** Based on geopolitical risk assessment, country-specific IP blocks from nations with elevated cyber threat activity have been included to enhance regional filtering aligned with compliance and organizational risk tolerance.

- **Regularly Updated and Validated:** This list is actively maintained and updated with the latest threat intelligence, ensuring continued relevance and effectiveness.

These changes ensure that SKYNET users benefit from a more targeted, effective, and manageable IP blocklist that enhances network defense and aligns with modern cybersecurity best practices.

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

This blocklist integrates and builds upon the incredible work by the [FireHOL IP Lists Project](https://github.com/firehol/blocklist-ipsets/), as well as additional threat intelligence from:
- Created with the assistance of [ChatGPT by OpenAI](https://openai.com/chatgpt), for automation, formatting, and research, published [here](https://chatgpt.com/share/683b750a-6be8-8000-a0e6-676a8a4a65c5) and [here](https://chatgpt.com/share/68444b4b-1d08-8000-a872-2dc9e6dd9841)

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/collingeorge/SKYNET/blob/main/LICENSE) file for details.

## Contribute

Have a trustworthy threat feed to recommend? Submit a pull request or open an issue.

## Support

Need help with .reg, .bat, .exe, or GPO/Intune deployment? Open an issue or PR, and assistance will be provided.
