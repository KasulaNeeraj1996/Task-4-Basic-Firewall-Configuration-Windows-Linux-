# Task 4 — Setup and Use a Firewall on Windows/Linux

## Option A — Linux (UFW: Uncomplicated Firewall)

### 1. Check firewall status
```bash
sudo ufw status verbose
```

### 2. Block port 23 (Telnet)
```bash
sudo ufw deny 23/tcp
```

### 3. Allow SSH (port 22)
```bash
sudo ufw allow 22/tcp
```

### 4. Remove block rule
```bash
sudo ufw delete deny 23/tcp
```

### 5. Reload firewall
```bash
sudo ufw reload
```

---

## Option B — Windows Firewall (GUI Method)

1. Open "Windows Defender Firewall with Advanced Security" from Control Panel or Start Menu.
2. Go to "Inbound Rules" → "New Rule".
3. Select "Port", choose "TCP", enter `23`, and choose "Block the connection".
4. Create another rule for port `22` to "Allow" SSH.
5. Delete the port 23 block rule to restore the original state.

---

## Testing the Rules

- On Linux, use:
```bash
telnet localhost 23
```
(Requires `telnet` client installed.)

- On Windows, enable the Telnet client from **Windows Features** and run:
```powershell
telnet localhost 23
```

If the firewall block is active, the connection should fail.

---

## Summary of Firewall Filtering

A firewall filters network traffic based on predefined rules for **ports**, **protocols**, and **IP addresses**.  
In this exercise:
- Port 23 (Telnet) was blocked to prevent insecure connections.
- Port 22 (SSH) was allowed for secure remote management.
