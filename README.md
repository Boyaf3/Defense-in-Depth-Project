# Defense-in-Depth Project

A comprehensive enterprise infrastructure security project demonstrating hacker-resistant enterprise architecture.

## Overview

This project implements defense-in-depth security architecture using:
- High-Availability firewalls with redundancy
- Encrypted DMVPN tunnels for secure communications
- Dynamic ARP inspection for network protection
- Inline Intrusion Prevention System (IPS)
- Strict network segmentation
- Centralized authentication

## Key Components

### Security Layers
1. **Perimeter Defense** - Redundant firewalls at network boundaries
2. **Encrypted Communications** - DMVPN secure tunnels
3. **Network Intelligence** - ARP inspection and threat detection
4. **Intrusion Prevention** - IPS blocking threats in real-time
5. **Access Control** - Centralized authentication

### Technologies Used
- High-Availability Firewalls
- DMVPN (Dynamic Multipoint VPN)
- Dynamic ARP Inspection (DAI)
- Intrusion Prevention System (IPS)
- Network Segmentation (VLANs)
- Centralized Authentication (LDAP/AD)

## Network Design

### Network Segments
- **DMZ** - Public-facing services
- **Internal Network** - Trusted resources
- **Management Network** - Administrative access
- **WAN Links** - Simulated internet connectivity

### Devices Included
- Firewalls (primary/secondary pair)
- Core and edge routers
- Distribution and access switches
- Authentication servers
- IPS appliance
- Monitoring and logging servers

## Getting Started with EVE-NG

### What is EVE-NG?

EVE-NG (Emulation Virtual Environment) is a free, open-source network emulation platform that lets you:
- Design and simulate complex network topologies
- Test configurations before production deployment
- Support multiple vendors (Cisco, Juniper, Fortinet, Palo Alto, etc.)
- Access devices via console
- Visualize network diagrams

### Prerequisites

- EVE-NG Community Edition installed
- Web browser access to EVE-NG interface
- The Defense-in-Depth topology file

## Importing Topology into EVE-NG

### Step 1: Access EVE-NG Web Interface

Open your web browser and navigate to:
```
http://<your_eve_ng_ip>:8080
```

Login with credentials (default: admin / eve)

### Step 2: Upload Topology File

1. In the EVE-NG web interface, click **"File Manager"** in the left sidebar
2. Navigate to the **topologies** folder
3. Upload the Defense-in-Depth topology file (`.unl`, `.json`, or `.yaml` format)
4. Wait for the upload to complete

### Step 3: Load the Topology

1. Go to **"Open Lab"** or **"Topologies"** section
2. Find and click the Defense-in-Depth topology file
3. The lab will load with all devices and networks

### Step 4: Start the Lab

1. Click **"Start all"** button to power on all devices
2. Wait for devices to boot (this takes a few minutes)
3. Check device status - should all show green (running)

### Step 5: Verify Everything Works

1. Right-click on each device → select **"Console"**
2. Verify device CLI access is working
3. Check network connections in the topology diagram
4. Confirm all links are connected

## Using the Topology

### Access Devices

**Via Web Console:**
- Click device → Select "Console"
- Device CLI opens in new window
- Full access to device commands

**Via SSH (if configured):**
- Note device management IP
- `ssh admin@<device_ip>`
- Use device credentials

### What You Can Test

- **Firewall rules** - Configure policies between zones
- **DMVPN tunnels** - Monitor encrypted connections
- **Network segmentation** - Test traffic filtering
- **High availability** - Simulate device failures
- **Authentication** - Test user access controls
- **IPS detection** - Configure and test security rules

## Topology Details

### Device Types

| Component | Role |
|-----------|------|
| Firewalls | Perimeter security & zone enforcement |
| Routers | DMVPN hub/spoke, core routing |
| Switches | VLAN segmentation, access switching |
| Auth Servers | LDAP/Active Directory services |
| IPS | Threat detection & prevention |
| Monitoring | Logs, alerts, dashboard |

### Network Layout

```
Internet (WAN)
    ↓
Primary Firewall ← → Secondary Firewall (HA)
    ↓
Switches
    ├─→ DMZ (External services)
    ├─→ Internal Network (Users/Resources)
    └─→ Management Network (Admin access)
```
## Best Practices

### Security
- Regularly update firewall rules
- Monitor IPS alerts and logs
- Test authentication regularly
- Keep configurations documented
- Enable all logging features

### Operations
- Maintain firewall redundancy
- Test failover regularly
- Monitor tunnel status
- Review logs weekly
- Backup configurations often

### Lab Usage
- Test changes before production
- Document all configurations
- Keep topology updated
- Use for training purposes
- Test incident response

## Use Cases

- Enterprise security architecture design
- Security team training
- Configuration testing
- Incident response practice
- Compliance requirement validation
- Network simulation before deployment

## Next Steps

1. **Import the topology** following the steps above
2. **Start the lab** and verify all devices boot
3. **Access each device** via console
4. **Review configurations** on firewalls and routers
5. **Test security policies** and rule enforcement
6. **Document findings** and configuration changes

## Support & Resources

- EVE-NG Documentation: https://www.eve-ng.net/
- Vendor documentation for your devices
- This project repository for configuration examples

## Author

Boyaf3

