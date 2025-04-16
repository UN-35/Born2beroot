# Born2beroot


<img align="center" src="https://w.wallhaven.cc/full/57/wallhaven-57joz1.png" />


## 🖥️ System Administration Project

This repository contains documentation for my implementation of the Born2beRoot project, a system administration exercise focused on setting up a secure virtual machine according to specific requirements.

![Virtual Machine](https://img.shields.io/badge/Virtual%20Machine-Debian/Rocky-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📝 Project Overview

Born2beRoot introduces the fundamentals of system administration through virtualization. The project requires creating a virtual machine using VirtualBox or UTM with either Debian or Rocky Linux. Through this exercise, I learned about:

- Virtual machine setup and configuration
- Operating system installation without GUI
- Implementing strong security policies
- Disk partitioning with LVM and encryption
- Network and service configuration
- User and group management
- System monitoring

## 📋 Key Requirements Implemented

### Base Configuration
- Set up a minimal server environment with no graphical interface
- Created encrypted LVM partitions
- Configured system security with AppArmor (Debian) / SELinux (Rocky)

### Security Measures
- Implemented SSH service on port 4242 only with root login disabled
- Configured UFW/firewalld allowing only necessary connections
- Set up strong password policies:
  - 30-day password expiration
  - 2-day minimum before password changes
  - 7-day warning before expiration
  - Minimum 10 characters with uppercase, lowercase, and numbers
  - No more than 3 consecutive identical characters
  - Password cannot contain username

### User Management
- Created user in the required groups (user42 and sudo)
- Implemented strict sudo rules:
  - Limited to 3 authentication attempts
  - Custom error message
  - Full action logging in /var/log/sudo/
  - TTY mode enabled
  - Restricted sudo paths

### Monitoring
- Developed the monitoring.sh script to display system information:
  - Architecture and kernel version
  - Physical/virtual processor information
  - Memory and disk usage statistics
  - System load and boot time
  - LVM status
  - Network information
  - User and sudo command statistics

## 📚 Repository Structure

**Note:** According to project requirements, this repository only contains the signature.txt file for submission. The structure below represents what would typically be included in a complete project repository for reference purposes:

```
Born2beRoot/
├── README.md                 # This documentation file
├── signature.txt             # The only required submission file - contains VM disk signature
│
├── [monitoring.sh]           # System monitoring script (not included - would exist on VM)
│
├── [config_files/]           # Directory for configuration files (not included)
│   ├── [sshd_config]         # SSH server configuration
│   ├── [sudoers]             # Sudo configuration
│   ├── [login.defs]          # Password policy settings
│   ├── [pam.d/]              # PAM configuration files
│   └── [ufw_status.txt]      # Firewall rules
│
├── [documentation/]          # Additional documentation (not included)
│   ├── [setup_guide.md]      # Installation and configuration steps
│   ├── [defense_prep.md]     # Notes for defense preparation
│   └── [screenshots/]        # Visual documentation of the setup
│       ├── [partitions.png]  # LVM partition layout
│       └── [monitoring.png]  # Monitoring script output
```

## 🔍 What I Learned

- System administration fundamentals
- Security best practices for Linux servers
- Service configuration and management
- User authentication and permission management
- Linux command line proficiency
- Virtualization concepts
- Partitioning and logical volume management
- System monitoring techniques

## ⚠️ Important Notes

1. As per project guidelines, the actual virtual machine is NOT included in this repository
2. Only the signature.txt file is required for submission
3. Other files mentioned in the structure are not physically present but represent what would be found on the virtual machine

## 🚀 Project Submission

To submit this project:
1. Create the virtual machine following all specifications
2. Generate the SHA1 signature of your VM disk file
3. Create a signature.txt file containing only this signature
4. Add the signature.txt file to this repository
5. Submit for evaluation

---

*This project is part of the curriculum at [1337](https://1337.ma).*
