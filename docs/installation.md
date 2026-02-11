---

# 🛠️ PART 1️⃣: Install Splunk Enterprise on Kali Linux

## Step 1: Download Splunk Enterprise

```bash
cd ~/Downloads
wget -O splunk-10.0.2-linux-amd64.deb \
https://download.splunk.com/products/splunk/releases/10.0.2/linux/splunk-10.0.2-e2d18b4767e9-linux-amd64.deb
```

---

## Step 2: Install Splunk

```bash
sudo dpkg -i splunk-10.0.2-linux-amd64.deb
```

If dependencies fail:

```bash
sudo apt --fix-broken install -y
```

---

## Step 3: Start Splunk & Accept License

```bash
sudo /opt/splunk/bin/splunk start --accept-license
```

Set:

- **Username:** admin  
- **Password:** @Splunk123  

---

## Step 4: Enable Splunk at Boot

```bash
sudo /opt/splunk/bin/splunk enable boot-start
```

---

## Step 5: Open Required Ports (Kali)

| Purpose        | Port |
|---------------|------|
| Web UI        | 8000 |
| Log Receiving | 9997 |
| Management    | 8089 |

```bash
sudo ufw allow 8000
sudo ufw allow 9997
sudo ufw allow 8089
```

---

## Step 6: Access Splunk Web

From browser:

```
http://<KALI_IP>:8000
```

Login as **admin**.
