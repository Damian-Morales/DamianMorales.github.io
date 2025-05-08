# Cybersecurity Incident Report – TCP SYN Flood Attack Analysis

**WireShark TCP/HTTP log:**
https://docs.google.com/spreadsheets/d/1enpRzrIao3J2Lp2tOI0hmu1Cu7D7CjLGhFAiTiR9J64/edit?gid=1522826613#gid=1522826613

## Section 1: Identify the Type of Attack That May Have Caused This Network Interruption

**One potential explanation for the website's connection timeout error message is:**

The company’s web server was targeted by a TCP SYN Flood Attack, a type of Denial-of-Service (DoS) attack. This occurs when a malicious actor sends a large volume of TCP SYN requests to initiate a handshake but never completes the connection.

**The logs show that:**

A high number of SYN requests were received from a suspicious IP address. These requests overwhelmed the server and were never completed, causing the server’s resources to decline and preventing authorized user access.

**This event could be:**

A DoS attack, more specifically a SYN Flood, where the attacker aims to drain server resources and make the website unavailable.

---

## Section 2: Explain How the Attack Is Causing the Website to Malfunction

When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol:

1. **SYN** – The client sends a synchronization packet to initiate the connection.
2. **SYN-ACK** – The server responds with a synchronization acknowledgment.
3. **ACK** – The client acknowledges the response and completes the connection.

**What happens when a malicious actor sends a large number of SYN packets all at once:**

The attacker sends SYN packets but never completes the handshake with an ACK. This causes the server to hold numerous half-open connections, draining available resources and leaving it unable to respond to requests.

**What the logs indicate and how that affects the server:**

The network logs show repeated SYN packets from a suspicious IP address with no follow-up ACK responses. This pattern is characteristic of a SYN Flood attack. The server becomes overwhelmed, cannot establish new connections, and ultimately times out everyone.

---

## Summary

- **Attack Type**: TCP SYN Flood (Denial-of-Service)
- **Impact**: Web server overwhelmed, resulting in connection timeouts and service unavailability
- **Evidence**: Wireshark/TCP log showing repeated SYNs without ACKs
- **Recommendation**:
  - Enable SYN cookies to protect against half-open connections
  - Implement afirewall rule to temporarily block the source IP
  - Monitor for potential IP spoofing or DDoS attacks
