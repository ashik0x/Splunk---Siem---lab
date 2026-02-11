# PART 4️⃣: Configure Windows Log Collection

---

## Step 11: Create inputs.conf

Navigate to:

C:\Program Files\SplunkUniversalForwarder\etc\system\local\

Create a new file named:

inputs.conf

Paste the following configuration:

```ini
[WinEventLog://Application]
index=windows
disabled=0

[WinEventLog://Security]
index=windows
disabled=0

[WinEventLog://System]
index=windows
disabled=0

[WinEventLog://Microsoft-Windows-Sysmon/Operational]
index=sysmon
disabled=0
renderXml=true

[WinEventLog://Microsoft-Windows-PowerShell/Operational]
index=powershell
disabled=0
renderXml=true

[WinEventLog://Windows PowerShell]
index=powershell
disabled=0
```

---

## Step 12: Restart Universal Forwarder

Open **Command Prompt as Administrator**

Run:

```bash
cd "C:\Program Files\SplunkUniversalForwarder\bin"
splunk restart
```

---

## Step 13: Allow Windows Firewall

Run:

```bash
netsh advfirewall firewall add rule name="Splunk UF" dir=out action=allow protocol=TCP remoteport=9997
```

---

✔️ Windows logs are now forwarding to Splunk.
