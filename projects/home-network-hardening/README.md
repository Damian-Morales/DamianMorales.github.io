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
- UPnP, WPS, and Remote Management were all disabled, minimizing unnecessary external exposure.
- WPA2 encryption is active on both Wi-Fi bands.
- The admin password is custom and secure, reducing credential-based risk.
- Firmware updates are handled automatically by the ISP (Spectrum), ensuring the router remains patched.

This step confirms that the current configuration provides a solid security foundation for further hardening actions.

## Step 3: Hardening Actions

After reviewing the router configuration, I applied additional security improvements to enhance the protection of the home network.

### Security Enhancements Applied
| Action | Description | Result |
|--------|--------------|--------|
| Enabled System Logging | Activated router logging to track activity and potential threats | Completed |
| Verified Firewall | Confirmed firewall is active and set to restrict unauthorized access | Completed |
| Disabled Port Forwarding | Prevented applications from opening inbound connections | Completed |
| Disabled DMZ | Stopped direct external access to internal devices | Completed |
| Reviewed Connected Devices | Verified all connected systems are recognized and trusted | Completed |
| Secure DNS | ISP-managed; Spectrum automatically provides secure DNS resolution | Not configurable manually |

### Screenshots
![Enable Logging](screenshots/Enable%20Logging%20(hardening).png)
![Firewall Status](screenshots/Firewall%20Status%20(hardening).png)
![Port Forwarding Disabled](screenshots/Port%20Forwarding%20disabled%20(hardening).png)
![DMZ Disabled](screenshots/DMZ%20disabled%20(hardening).png)
![Connected Devices](screenshots/Connected%20Devices%20(hardening).png)

### Summary
The router was successfully hardened by enabling monitoring, verifying the firewall, and disabling risky features such as DMZ and Port Forwarding.  
All connected devices were confirmed to be legitimate, and DNS resolution is securely managed by the ISP.  
These actions significantly reduce attack surfaces and strengthen the overall resilience of the home network.

## Step 4: Conclusion & Recommendations

Through this project, I conducted a comprehensive security review and hardening of my home network.  
Each step—from initial mapping to configuration auditing—helped identify and mitigate potential vulnerabilities commonly found in consumer routers.

### Summary of Achievements
- Logged into the router’s admin interface and reviewed current settings  
- Disabled insecure features such as UPnP, WPS, and DMZ  
- Verified WPA2 encryption and confirmed strong Wi-Fi passwords  
- Enabled system logging for ongoing monitoring  
- Verified firewall protection was active  
- Ensured all connected devices were recognized and trusted  

### Recommendations for Ongoing Security
1. Check for firmware updates monthly to ensure the router remains protected against new vulnerabilities.  
2. Change Wi-Fi passwords periodically (at least every 6 months).  
3. Monitor the router logs for repeated failed login attempts or unknown IP addresses.  
4. Add network segmentation in the future (e.g., a guest Wi-Fi network for visitors).  
5. Consider using a separate hardware firewall or intrusion-detection device for layered protection.  

### Final Reflection
This project strengthened both my practical understanding of home-network security and my ability to perform a real-world configuration audit.  
By applying cybersecurity principles such as least privilege, visibility, and defense-in-depth, I reduced the attack surface and improved the overall resilience of my network.  
These are the same techniques that can be applied to small-business and enterprise environments to ensure a secure network baseline.

