# ☁️ SKYNET Blocklist

**SKYNET** is a malware IP blocklist management tool designed to enhance your network security by blocking inbound and outbound connections to known malicious hosts.

This repository contains a curated blocklist that integrates with the [SKYNET](https://github.com/collingeorge/SKYNET) system to block malware communications, with a strong emphasis on **outbound** control to disrupt command-and-control (C2) traffic.

---

## 🔄 How to Use

### Step 1: Update the Blocklist

1. Launch the **SKYNET** interface.
2. Choose **Option 3** (Update Blocklist).
3. Enter the following blocklist URL:
```
https://raw.githubusercontent.com/collingeorge/SKYNET/refs/heads/main/blocklist
```


---

### Step 2: Disable CDN Whitelisting

To improve effectiveness and prevent bypass:

1. In the **SKYNET** main menu, choose **Option 11**.
2. Disable **CDN Whitelisting**.

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
