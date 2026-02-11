# PART 2️⃣: Configure Splunk to Receive Logs

## Step 7: Enable Receiving Port

Splunk Web →
Settings → Forwarding & Receiving → Configure Receiving → New

Port: 9997

Save

✔️ Splunk is now ready to receive logs


## Step 8: Create Required Indexes (IMPORTANT)

Splunk Web →
Settings → Indexes → New Index

Create three indexes:

windows
sysmon
powershell

⚠️ Indexes must exist BEFORE logs are received
