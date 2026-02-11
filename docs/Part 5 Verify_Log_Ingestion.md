# PART 5️⃣: Verify Log Ingestion

---

## Step 14: Check Forwarder Connection

Go to:

Splunk Web → Settings → Forwarder Management

✔️ Your Windows host should appear in the list.

---

## Step 15: Search Logs in Splunk

### View All Logs
```
index=*
```

### Windows Logs
```
index=windows
```

### Login Success / Failure
```
index=windows EventCode=4624 OR EventCode=4625
```

### Sysmon Process Creation
```
index=sysmon EventCode=1
```

### Sysmon Network Connections
```
index=sysmon EventCode=3
```

### PowerShell Execution
```
index=powershell EventCode=4104
```

---

# ✅ Validation Checklist

| Log Type              | Event Code |
|-----------------------|------------|
| Login Success         | 4624       |
| Login Failure         | 4625       |
| Sysmon Process        | 1          |
| Sysmon Network        | 3          |
| PowerShell Script     | 4104       |

✔️ If you see these logs → Lab is working correctly.

---

# 🛠️ Common Issues & Fixes

## ❌ No Logs Received
- ✔️ Check Kali IP address
- ✔️ Ensure port 9997 is enabled
- ✔️ Confirm both VMs use same network adapter

## ❌ Security Logs Missing
- ✔️ Run Universal Forwarder as Administrator
- ✔️ Ensure Windows Security log is enabled

## ❌ Firewall Blocking
- ✔️ Temporarily disable firewall for testing
- ✔️ Re-enable after validation
