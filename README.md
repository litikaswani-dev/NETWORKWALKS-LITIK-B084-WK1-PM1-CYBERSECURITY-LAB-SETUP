# 🛡️ Cybersecurity Lab Setup

A beginner-friendly cybersecurity lab environment built using **Kali Linux** and **Oracle VirtualBox**. This project documents the installation, configuration, and verification of a virtual machine for cybersecurity learning and practical exercises.

## 📌 Project Overview

The goal of this project is to create an isolated virtual environment where cybersecurity tools and networking concepts can be explored safely without making changes to the host operating system.

This repository documents the initial lab setup, including virtual machine configuration, network configuration, connectivity testing, and evidence screenshots.

## 🧰 Tools & Technologies

- **Kali Linux 2026.3** – Linux distribution for cybersecurity and penetration testing.
- **Oracle VirtualBox** – Virtualization software used to run Kali Linux.
- **Windows 11** – Host operating system.
- **VirtualBox NAT Network** – Provides network connectivity to the virtual machine.
- **Linux Terminal & Windows CMD** – Used for configuration and verification.

## ⚙️ Virtual Machine Configuration

| Setting | Configuration |
|---|---|
| Operating System | Kali Linux 2026.3 (64-bit) |
| Virtualization | Oracle VirtualBox |
| RAM | 2048 MB |
| CPUs | 2 |
| Network Adapter | NAT Network |
| NAT Network Name | `NatNetwork` |
| Shared Clipboard | Bidirectional |
| Drag and Drop | Bidirectional |
| Shared Folder | Windows Downloads folder |

## 🌐 Network Configuration

The Kali virtual machine uses a NAT Network named `NatNetwork`.

| Network Setting | Value |
|---|---|
| Network Address | `10.0.0.0/24` |
| Kali Static IP | `10.0.0.2/24` |
| Default Gateway | `10.0.0.1` |
| DHCP Server | `10.0.0.254` |
| DHCP Address Range | `10.0.0.3 – 10.0.0.253` |
| DNS Servers | `1.1.1.1`, `1.0.0.1` |

The Kali virtual machine was assigned a static IP address, while the VirtualBox NAT Network provides DHCP configuration for other devices on the network.

## ✅ Connectivity Verification

Network connectivity was tested using the following commands in Kali Linux:

**1. Check the gateway connection**
```bash
ping -c 4 10.0.0.1
```

**2. Check internet connectivity using an IP address**
```bash
ping -c 4 8.8.8.8
```

**3. Check DNS resolution and internet connectivity**
```bash
ping -c 4 google.com
```

All three tests completed successfully, with **4 packets received and 0% packet loss** in each test.

## 📸 Evidence & Screenshots

The `screenshots/` directory contains evidence of the lab configuration and successful verification.

| Screenshot | Description |
|---|---|
| `01-dhcp-configuration.png` | VirtualBox DHCP configuration |
| `02-kali-ip-configuration.png` | Kali IP address and routing configuration |
| `03-connectivity-tests.png` | Successful gateway, internet, and DNS connectivity tests |
| `04-kali-snapshot.png` | VirtualBox snapshot of the configured Kali VM |
| `05a-nat-network-dhcp.png` | Detailed NAT Network DHCP configuration |
| `05b-1-kali-vm-hardware-network.png` | VM hardware and network settings |
| `05b-2-kali-vm-integration.png` | Shared clipboard, drag and drop, and shared folder settings |

## 💾 Virtual Machine Snapshot

A VirtualBox snapshot named **`Week1 - Working Lab Setup`** was created after completing the initial configuration.

This snapshot provides a restore point that can be used to return the virtual machine to its working state if future experiments cause configuration issues.

## 📁 Repository Structure

```text
cybersecurity-lab-setup/
│
├── screenshots/
│   ├── 01-dhcp-configuration.png
│   ├── 02-kali-ip-configuration.png
│   ├── 03-connectivity-tests.png
│   ├── 04-kali-snapshot.png
│   ├── 05a-nat-network-dhcp.png
│   ├── 05b-1-kali-vm-hardware-network.png
│   └── 05b-2-kali-vm-integration.png
│
└── README.md
```

## 🎯 Learning Objectives

Through this initial setup, I gained practical experience with:

- Setting up and configuring a Kali Linux virtual machine.
- Understanding virtualization and virtual machine resources.
- Configuring NAT networking in VirtualBox.
- Assigning a static IP address and understanding DHCP.
- Understanding default gateways and DNS servers.
- Testing network connectivity using Linux commands.
- Configuring shared folders between a host and guest operating system.
- Creating and managing virtual machine snapshots.

## 🚀 Future Work

This repository will serve as the foundation for future cybersecurity lab exercises, including networking, reconnaissance, vulnerability assessment, and other practical security concepts.

## 📚 References

- [Kali Linux Official Website](https://www.kali.org/)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Kali Linux in VirtualBox](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/)
- [Oracle VirtualBox](https://www.virtualbox.org/)

---

**Disclaimer:** This lab is intended for educational purposes. Any security testing should only be performed on systems and networks for which permission has been granted.
