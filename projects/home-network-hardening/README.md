# Home Network Security Hardening Project

## Overview
This project focuses on **improving the security posture of a typical home network** by identifying vulnerabilities, hardening connected devices, and documenting best practices for secure configurations.

The goal is to **reduce attack surface**, **increase visibility**, and **develop a systematic process** for maintaining network security at home.

---

## Project Setup
1. **Create a new directory for documentation and screenshots**
   ```bash
   mkdir screenshots
   
## Step 1: Network Mapping

To begin the hardening process, I logged into my router’s local web interface (192.168.1.1) to document network topology and connected devices.

### Key Information Collected
- **Router Model & Firmware:** Helps verify that the device is up to date with the latest vendor patches.  
- **Wireless Settings:** Shows encryption mode (WPA2/WPA3) and SSID configuration.  
- **Connected Devices:** Lists all active endpoints on the LAN and Wi-Fi networks.  
- **DHCP Configuration:** Identifies internal IP range and lease time.

### Screenshots
![Router Info](screenshots/Router%20model%20and%20firmware%20version%20(router).png)
![Wireless Settings](screenshots/Wireless%20Settings%20(router).png)
![Connected Devices](screenshots/Connected%20Devices%20(router).png)
![DHCP Info](screenshots/LAN%20IP%20and%20DHCP%20Range%20(router).png)

This establishes a baseline of the home network layout for further hardening.


## Step 2: Router Security Assessment

After mapping the network, I performed a router security audit to assess configurations, identify potential weaknesses, and ensure strong security settings were in place.

### Security Review Checklist

| Category | Setting Checked | Status | Recommendation |
|-----------|----------------|--------|----------------|
| Remote Management | Access from WAN | Disabled | ✅ Secure |
| UPnP | Automatic port configuration | Disabled | ✅ Secure |
| WPS | Wi-Fi Protected Setup | Disabled | ✅ Secure |
| Admin Credentials | Default password changed | Yes | ✅ Secure |
| Wireless Security | WPA2 Enabled | Yes | ✅ Secure |
| Guest Network | Not detected / Disabled | ✅ Secure |
| Firmware | Up to date (ISP-managed) | Yes | ✅ Secure |

### Screenshots
![UPnP](screenshots/Universal%20Plug%20and%20Play%20(security).png)
![WPS](screenshots/WPS%20is%20off%20(security).png)
![WPA2](screenshots/WPA2%20being%20used%20(security).png)
![Admin](screenshots/admin%20username%20(security).png)
![Firmware](screenshots/Check%20Firmware%20(security).png)

### Findings Summary
The router showed strong baseline security:
- **UPnP**, **WPS**, and **Remote Management** were all disabled, minimizing unnecessary external exposure.
- **WPA2 encryption** is active on both Wi-Fi bands.
- The **admin password** is custom and secure, reducing credential-based risk.
- **Firmware** updates are handled automatically by the ISP (Spectrum), ensuring the router remains patched.

This step confirms that the current configuration provides a solid security foundation for further hardening actions.
