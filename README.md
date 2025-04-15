# Linux Training Plan for Kubernetes and Cybersecurity

## Overview
This training plan is designed for a network architect with 15+ years of experience, CCIE in Routing and Switching, LPI Linux Essentials certification, and experience using Ubuntu for Python development, Docker, Git, and various IDEs. The goal is to enhance Linux skills specifically for Kubernetes and cybersecurity/penetration testing.

## Time Commitment
- Weekdays: 1-2 hours per day
- Weekends: 3-4 hours per day

## 12-Week Roadmap

### Weeks 1-2: Linux System Administration Fundamentals
### Weeks 3-4: Linux Networking and Security Fundamentals
### Weeks 5-6: Linux Security Hardening
### Weeks 7-8: Containerization and Kubernetes Foundations
### Weeks 9-10: Advanced Kubernetes on Linux
### Weeks 11-12: Linux Penetration Testing

## Recommended Certifications
1. **Linux Professional Institute LPIC-1**
2. **Certified Kubernetes Administrator (CKA)**
3. **CompTIA Linux+ and Security+**
4. **Offensive Security Certified Professional (OSCP)** (longer-term goal)

---
## Pre-Setup Day (Before Week 1)
**Focus: Setting Up Cloud-Based Linux Practice Environments**

### Option 1: Free Browser-Based Linux Terminals (No Installation Required)
- **[JSLinux](https://bellard.org/jslinux/)** - Run Linux directly in your browser
  - Pro: Instant access, no signup required
  - Con: Session not persistent between browser refreshes
  - Setup: Simply visit the website and select a Linux distribution

- **[Killercoda Ubuntu Playground](https://killercoda.com/playgrounds/scenario/ubuntu)**
  - Pro: Full Ubuntu terminal with root access
  - Con: Sessions last only 1 hour
  - Setup: Visit the website, no account required

- **[TryHackMe](https://tryhackme.com/)** - Interactive cybersecurity training platform
  - Pro: Provides full Linux VMs with graphical interface via browser
  - Con: Requires free account registration
  - Setup: 
    1. Create a free account
    2. Join rooms like "Linux Fundamentals" 
    3. Start the machine in the room and access via browser

### Option 2: Cloud-Based Virtual Machines

- **[Oracle Cloud Free Tier](https://www.oracle.com/cloud/free/)**
  - Pro: Always Free tier includes 2 Linux VMs that never expire
  - Con: Requires credit card for signup (but no charges for Always Free resources)
  - Setup:
    1. Sign up for Oracle Cloud account
    2. Create an "Always Free" Compute instance
    3. Select Ubuntu or CentOS
    4. Access via SSH

- **[Google Cloud Platform Free Tier](https://cloud.google.com/free)**
  - Pro: Includes e2-micro VM instances in Free Tier
  - Con: Requires credit card for signup
  - Setup:
    1. Sign up for GCP account
    2. Create a VM instance using e2-micro (eligible for Free Tier)
    3. Select Ubuntu as the operating system
    4. Access via Cloud Shell or SSH

### Option 3: Local Options Without Full VM Installation

- **Docker Container**
  - Pro: Lightweight, starts instantly
  - Con: Requires Docker installation 
  - Setup:
    ```bash
    # Pull and run Ubuntu container
    docker run -it ubuntu bash
    
    # For persistent storage, use volumes
    docker run -it -v ~/linux_practice:/workspace ubuntu bash
    ```

- **Windows Subsystem for Linux (WSL)** (For Windows Users)
  - Pro: Integrated with Windows, easy to use
  - Con: Some system-level operations may differ from a standard Linux installation
  - Setup:
    1. Open PowerShell as Administrator
    2. Run `wsl --install` (for Windows 11) or follow Microsoft's guide for Windows 10
    3. Restart and complete Ubuntu setup

### Recommended Setup for This Training Plan

For the most consistent experience with this training plan, we recommend:

1. **Primary Option**: TryHackMe's Linux Fundamentals rooms (Linux Fundamentals 1 is free, all others require Premium)
   - Complete environment with all necessary tools
   - Designed specifically for learning
   - Interactive exercises align with our training goals

2. **Backup Option**: Oracle Cloud Free Tier VM 
   - Persistent environment available 24/7
   - Full control over the system for advanced exercises
   - Good preparation for working in cloud environments

Before proceeding to Week 1, choose and set up at least one of these environments to ensure you're ready for the daily exercises.
