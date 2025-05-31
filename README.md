# ☁️ SKYNET Blocklist

**SKYNET** is a firewall that was built by Adam00. The project is found here:

https://github.com/Adamm00/IPSet_ASUS

This repository is to dedicated to the development, testing and sharing of better blocklists and settings of SKYNET. This malware IP blocklist is designed to enhance your network security by blocking inbound and outbound connections to known malicious hosts, with a strong emphasis on **outbound** control to disrupt command-and-control (C2) traffic.

---

## 🔄 How to Use

### Step 1: Update the Blocklist

1. Launch the **SKYNET** interface.
2. Choose **Option 3** ("Malware Blacklist").
3. Choose **Option 2** ("Change filter list").
4. Enter the following blocklist URL:
```
https://raw.githubusercontent.com/collingeorge/SKYNET/refs/heads/main/blocklist
```


---

### Step 2: Disable CDN Whitelisting

To improve effectiveness and prevent malware and command and control network bypasses:

1. In the **SKYNET** main menu, choose **Option 11** (Settings).
2. Choose **Option 14** ("CDN Whitelisting").
3. Choose **Option 2** ("Disable").

---

### ✅ What to Expect

- Allow SKYNET to run for **at least 24 hours**.
- After this period, log in and check block statistics.
- You should begin to see **both inbound and outbound** IPs being blocked.

> Outbound blocks are **especially valuable**, as they can stop malware from connecting to external control servers (C2 infrastructure).

---

## 🙌 Credits

This blocklist integrates and builds upon the incredible work by the [FireHOL IP Lists Project](https://github.com/firehol/blocklist-ipsets/).

---

## 📄 License

This repository follows the original licensing of the included blocklists. Please refer to the source project ([FireHOL](https://github.com/firehol/blocklist-ipsets/)) for attribution and usage rights.

---

## 🛠️ Contributions

PRs welcome — if you'd like to submit improvements or add additional threat intel feeds, feel free to open a pull request!
