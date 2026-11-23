
# Network Security & SIEM Implementation

**Network Security | Intrusion Detection | SIEM Monitoring | Blue Team**

A hands-on cybersecurity project focused on network defense, intrusion detection, centralized security monitoring, and security testing within a VMware-based virtual infrastructure.

The project integrates **pfSense, Suricata IDS, Elasticsearch, Kibana, Winlogbeat, and Kali Linux** to establish a multi-layered network security and monitoring environment.

## Project Overview

The project demonstrates the configuration and integration of network security technologies across six virtual machines.

The environment supports network segmentation, firewall policy enforcement, intrusion detection, Windows event collection, and centralized security monitoring.

### Core Capabilities

- Network segmentation and firewall administration
- Intrusion detection and security alert generation
- Centralized Windows event monitoring
- Security event analysis and visualization
- Network reconnaissance detection
- Controlled security testing and validation

## Technology Stack

| Category | Technologies |
|---|---|
| Virtualization | VMware |
| Firewall & Routing | pfSense 2.8.1 |
| Intrusion Detection | Suricata IDS, Emerging Threats |
| SIEM | Elasticsearch, Kibana |
| Log Collection | Winlogbeat, Filebeat |
| Security Testing | Kali Linux, Nmap |
| Operating Systems | Ubuntu, Windows 10, Windows Server 2019 |

## Network Architecture

The infrastructure consists of segmented virtual networks managed by pfSense.

| Component | IP Address | Role |
|---|---|---|
| Kali Linux | 10.10.3.20 | Security testing |
| Windows 10 | 10.10.2.21 | Monitored endpoint |
| Elastic Stack | 10.10.2.23 | SIEM server |
| pfSense LAN1 | 10.10.2.10 | Firewall gateway |

### Windows Event Monitoring

```text
Windows Event Logs
        |
        v
    Winlogbeat
        |
        v
  Elasticsearch
        |
        v
      Kibana
```

### Network Intrusion Detection

```text
Kali Linux (LAN2)
        |
        v
   Network Traffic
        |
        v
  pfSense Firewall
        |
        v
   Suricata IDS
        |
        v
 Security Alerts
    / EVE JSON
```

## Key Implementations

### 1. Firewall Configuration — pfSense

- Configured virtual network interfaces and routing.
- Implemented firewall rules for segmented networks.
- Configured access restrictions for RDP traffic.
- Validated network policies using Nmap and connectivity tests.

### 2. Intrusion Detection — Suricata IDS

- Deployed Suricata on the LAN2 interface.
- Configured Emerging Threats detection signatures.
- Created a custom Nmap scanning detection rule.
- Monitored network reconnaissance alerts.
- Generated structured network events using EVE JSON.

### 3. SIEM Monitoring — Elastic Stack

- Deployed Elasticsearch and Kibana on Ubuntu.
- Configured Winlogbeat for Windows event forwarding.
- Centralized Windows security event collection.
- Analyzed security events through Kibana Discover.
- Used Kibana dashboards for security monitoring.

### 4. Security Testing & Validation

Performed controlled security tests covering:

- Network connectivity
- Nmap reconnaissance
- Firewall rule validation
- RDP access restrictions
- IDS alert generation
- Windows event collection
- SIEM monitoring and visualization

## Implementation Results

The environment demonstrated:

- Functional network segmentation and firewall enforcement.
- Filtered TCP/3389 access during Nmap testing.
- Suricata alerts identifying Nmap-related activity.
- Successful Winlogbeat communication with Elasticsearch.
- Centralized Windows event visibility in Kibana.
- Security event analysis through monitoring dashboards.

## Technical Documentation

The complete technical report contains network architecture, configuration details, implementation screenshots, security testing, and results.

**[View Full Technical Report (PDF)](Network_Security_and_SIEM_Implementation_Report.pdf)**

## Skills Demonstrated

`Network Security` `Firewall Configuration` `Suricata IDS` `SIEM` `Elastic Stack` `Log Analysis` `Security Monitoring` `Blue Team`

---

**Author:** Raul Isayev  
**Project Type:** Network Security & SIEM Implementation  
**Documentation:** Technical Portfolio / Case Study
