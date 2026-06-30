\# Project 01 - Enterprise Linux Server Initial Configuration



\## Ticket Information



| Item | Value |

|------|-------|

| Ticket ID | LNX-001 |

| Priority | Medium |

| Assigned Role | Junior Infrastructure Support Engineer |

| Status | Completed |



\---



\# Business Scenario



ABC Manufacturing required a new Ubuntu Server to serve as the foundation for future infrastructure services.



As the assigned Junior Infrastructure Support Engineer, my responsibility was to deploy, configure, secure, and verify the server according to company standards.



\---



\# Objectives



\- Deploy Ubuntu Server 24.04.4 LTS

\- Update the operating system

\- Create a dedicated administrator account

\- Configure sudo privileges

\- Install and configure OpenSSH Server

\- Configure multiple network interfaces

\- Enable remote administration

\- Verify successful deployment



\---



\# Environment



| Component | Details |

|----------|---------|

| Host Operating System | Windows 11 |

| Hypervisor | Oracle VirtualBox |

| Guest Operating System | Ubuntu Server 24.04.4 LTS |

| Remote Client | Windows PowerShell |

| SSH Server | OpenSSH |



\---



\# Network Configuration



| Adapter | Purpose |

|----------|----------|

| Adapter 1 | NAT (Internet Connectivity) |

| Adapter 2 | Host-Only (Remote Administration) |



\---



\# Implementation Summary



\- Performed initial system assessment.

\- Updated Ubuntu package repositories.

\- Upgraded installed packages.

\- Created a dedicated administrator account (`tmansuri`).

\- Added the administrator account to the `sudo` group.

\- Verified administrative privileges.

\- Verified OpenSSH Server installation.

\- Started the SSH service.

\- Enabled SSH to start automatically at boot.

\- Added a Host-Only network adapter in VirtualBox.

\- Configured Netplan to enable the second network interface.

\- Validated the Netplan configuration.

\- Applied the new network configuration.

\- Verified both network interfaces.

\- Successfully established an SSH connection from Windows PowerShell.



\---



\# Verification Commands



```bash

hostnamectl

ip addr

ip route

systemctl status ssh

groups tmansuri

who

```



\---



\# Engineering Decisions



| Decision | Reason |

|----------|--------|

| Created a dedicated administrator account | Avoid using the installation account for daily administration. |

| Granted sudo privileges instead of using the root account | Follows the Principle of Least Privilege. |

| Configured a Host-Only adapter | Enables secure management from the Windows host. |

| Backed up the Netplan configuration before editing | Allows quick recovery from configuration mistakes. |

| Validated Netplan before applying changes | Prevents network outages caused by syntax errors. |

| Used SSH for administration | Reflects how Linux servers are managed in production environments. |



\---



\# Skills Demonstrated



\- Linux System Administration

\- User Management

\- Linux Permissions

\- Sudo Administration

\- OpenSSH Configuration

\- Service Management (`systemd`)

\- Netplan Configuration

\- Linux Networking

\- Remote Administration

\- Infrastructure Troubleshooting



\---



\# Lessons Learned



\- Why operating systems should be updated before configuration.

\- Difference between starting and enabling a service.

\- Difference between NAT and Host-Only networking.

\- Importance of creating backups before modifying configuration files.

\- Importance of validating configurations before applying them.

\- Benefits of managing Linux servers remotely using SSH.



\---



\# Future Improvements



\- Configure UFW Firewall.

\- Implement SSH key-based authentication.

\- Disable root SSH login.

\- Configure Fail2Ban.

\- Apply basic SSH hardening.



\---



\# Project Outcome



Successfully deployed and configured an enterprise-style Ubuntu Server with secure remote administration, multi-interface networking, and documented implementation suitable for an Infrastructure Support Engineer portfolio.



\---



Project completed as part of the \*\*Linux Infrastructure Labs\*\* portfolio.

