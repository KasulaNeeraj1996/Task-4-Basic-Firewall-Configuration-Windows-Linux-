# Task 4 — Basic Firewall Configuration (Windows/Linux)

This repository contains all necessary files to complete Task 4: setting up and testing firewall rules to block or allow specific network traffic on Windows or Linux.

## 📌 Objective
- Configure a firewall using Windows Firewall or UFW (Uncomplicated Firewall) on Linux.
- Block and allow selected ports.
- Test rules to confirm they work.
- Document results with screenshots and configuration outputs.

## 📂 Repository Structure
- `docs/FIREWALL_SETUP_AND_USE.md` — step-by-step setup and usage guide.
- `sample_config/ufw_status_sample.txt` — fictional sample firewall configuration output.
- `screenshots/` — add real screenshots showing firewall rules applied.
- `templates/` — (optional) templates for documenting your firewall activity.

## 🚀 Quick Start
1. Follow `docs/FIREWALL_SETUP_AND_USE.md` for your OS.
2. Block port 23 (Telnet) and test using `telnet localhost 23`.
3. Allow port 22 (SSH) if on Linux.
4. Remove test block rule to restore original state.
5. Save terminal outputs/screenshots in `screenshots/` and configs in `sample_config/`.

## 🧪 Testing
- Linux: Use `telnet localhost 23` after blocking to verify connection is denied.
- Windows:Enable Telnet Client in Windows Features and test similarly.

## 📌 Notes
- The `ufw_status_sample.txt` provided here is fictional for reference.
- Do not block ports critical for your OS or active services without knowing the impact.
