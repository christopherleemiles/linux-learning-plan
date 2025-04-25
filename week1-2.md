# Linux Training Plan for Kubernetes and Cybersecurity - Weeks 1-2

## Setup Day
**Focus: Preparing Your Linux Learning Environment**

### Creating Your Linux Lab Environment
- Set up a Linux VM using VMware Workstation
  - Recommended distribution: Ubuntu Server 22.04 LTS (for main practice)
  - Optional second VM: CentOS/RHEL (for comparing different Linux distributions)
- Configure VM specifications:
  - At least 2GB RAM, 2 CPU cores
  - 20GB+ disk space
  - Enable nested virtualization if your hardware supports it
- Take a snapshot after base installation (for easy reset between labs)

### Alternative Lab Setup Approaches:
- Multi-VM setup for network practice:
  - Main admin VM + 1-2 target VMs for service deployment
  - Configure host-only network for inter-VM communication
- For later security exercises:
  - Consider adding a security-focused distribution VM (e.g., Kali Linux)
  - Set up a vulnerable VM for controlled penetration testing

With your environment prepared, each day will include:
1. Learning material for the topic
2. Hands-on lab exercises to apply what you've learned
3. Challenge tasks to test your understanding

## Week 1

### Monday (1-2 hours)
**Focus: File System Management Basics**

**Learning Material**:
- **Primary**: DigitalOcean Linux Filesystem Basics Tutorial
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-manage-files-and-directories-in-linux
- **Supplementary**: The Linux Documentation Project Guide
  - **Where to find**: https://tldp.org/LDP/intro-linux/html/sect_03_01.html
- **Interactive Reference**: Explainshell - Explains Linux commands
  - **Where to find**: https://explainshell.com/

**Lab Exercises**:
1. **Directory Exploration Lab**
   - Map out the main system directories (/etc, /var, /usr, etc.)
   - Document the purpose of each directory
   - Find which directories contain the most files/data using `du -sh /*`

2. **File Locating Lab**
   - Practice using `find` to locate:
     - All configuration files modified in the last day
     - Files larger than 10MB
     - Files with specific permissions
   - Use `grep` to search for specific content within files:
     - Find all files containing your username
     - Search for IP addresses in configuration files

**Challenge Task**:
- Create a shell script that maps your system's directory structure, showing the size and number of files in each main directory
- **Additional Resource**: Bash Scripting Tutorial
  - **Where to find**: https://linuxconfig.org/bash-scripting-tutorial-for-beginners

### Tuesday (1-2 hours)
**Focus: Advanced File Operations**

**Learning Material**:
- **Primary**: "The Linux Command Line" by William Shotts (freely available online)
  - **Where to find**: http://linuxcommand.org/tlcl.php (Chapters 7-9)
- **Supplementary**: GNU Coreutils Manual
  - **Where to find**: https://www.gnu.org/software/coreutils/manual/
- **Video Resource**: Learn Linux TV - Advanced File Management
  - **Where to find**: https://www.youtube.com/c/LearnLinuxtv

**Lab Exercises**:
1. **Text Processing Lab**
   - Create a log file with multiple entries
   - Extract specific information using grep with regular expressions
   - Format the output using awk and sed
   - Sort and filter the results

2. **File Archiving Lab**
   - Create a directory structure with various file types
   - Archive it using different methods:
     - tar without compression
     - tar with gzip compression
     - tar with bzip2 compression
   - Compare the resulting file sizes
   - Practice extraction to different locations

**Challenge Task**:
- Write a script that:
  1. Finds all log files in /var/log
  2. Extracts all ERROR messages
  3. Sorts them by date
  4. Creates a daily report
- **Additional Resource**: Regular Expression Testing Tool
  - **Where to find**: https://regex101.com/

### Wednesday (1-2 hours)
**Focus: User and Group Management**

**Learning Material**:
- **Primary**: DigitalOcean User Management Guide
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-add-and-delete-users-on-ubuntu-20-04
- **Supplementary**: Red Hat User/Group Management Documentation
  - **Where to find**: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_basic_system_settings/managing-users-groups-and-permissions_configuring-basic-system-settings
- **Interactive Practice**: TryHackMe - Linux Fundamentals Part 2
  - **Where to find**: https://tryhackme.com/room/linuxfundamentalspart2 (free account required)

**Lab Exercises**:
1. **User Administration Lab**
   - Create multiple users with different specifications:
     - Regular user with password
     - System user without login capability
     - User with specific home directory
   - Set password policies using chage
   - Understand /etc/passwd, /etc/shadow, and /etc/group files

2. **Group Management Lab**
   - Create groups for different purposes (e.g., developers, admins)
   - Add users to multiple groups
   - Set up a shared directory with group permissions
   - Change primary groups for users

**Challenge Task**:
- Create a secure collaboration environment:
  1. Set up three users with different roles
  2. Create shared directories with appropriate permissions
  3. Configure sudo access with specific command restrictions
- **Additional Resource**: Linux Permissions Calculator
  - **Where to find**: https://permissions-calculator.org/

### Thursday (1-2 hours)
**Focus: File Permissions and Access Control**

**Learning Material**:
- **Primary**: Red Hat's Guide to Linux File Permissions
  - **Where to find**: https://www.redhat.com/en/blog/linux-file-permissions-explained
- **Supplementary**: Baeldung on Linux: Setting Permissions with chown and chmod
  - **Where to find**: https://www.baeldung.com/linux/chown-chmod-permissions
- **Interactive Demo**: DigitalOcean's ACL Tutorial
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-use-acls-access-control-lists-on-linux

**Lab Exercises**:
1. **Basic Permissions Lab**
   - Create files with various permission combinations
   - Use numeric and symbolic notation to modify permissions
   - Understand the impact of different permissions on security
   - Practice with chmod, chown, and chgrp commands

2. **Advanced Access Control Lab**
   - Implement Access Control Lists (ACLs) for fine-grained permissions
   - Set up and use extended attributes
   - Understand and use special permissions (setuid, setgid, sticky bit)
   - Configure umask settings

**Challenge Task**:
- Design a secure file server setup:
  1. Create a directory structure for different departments
  2. Implement appropriate permissions and ACLs
  3. Test the security by attempting access as different users
- **Additional Resource**: SANS Institute File Permission Guide
  - **Where to find**: https://www.sans.org/blog/linux-cheat-sheet-for-pen-testers/

### Friday (1-2 hours)
**Focus: Package Management**

**Learning Material**:
- **Primary**: DigitalOcean APT Package Management Tutorial
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-manage-packages-in-ubuntu-and-debian-with-apt-get-apt-cache
- **Supplementary**: PackageCloud Blog on Linux Package Managers
  - **Where to find**: https://packagecloud.io/blog/what-is-a-linux-package-manager/
- **Reference for RPM**: Red Hat Package Management Guide
  - **Where to find**: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_software_with_the_dnf_tool/index

**Lab Exercises**:
1. **Package Management Fundamentals Lab**
   - Update package repositories
   - Install, upgrade, and remove packages
   - Search for packages by functionality
   - Lock package versions
   - Clean package caches

2. **Advanced Package Tasks Lab**
   - Download package files without installing
   - Examine package contents and dependencies
   - Configure package sources and priorities
   - Handle package conflicts

**Challenge Task**:
- Write a system audit script that:
  1. Lists all manually installed packages (non-dependencies)
  2. Identifies outdated packages
  3. Checks for security updates
  4. Creates a report with recommendations
- **Additional Resource**: LinuxConfig System Monitoring and Auditing Guide
  - **Where to find**: https://linuxconfig.org/monitoring-and-auditing

### Weekend (6-8 hours total)

**Saturday: VM Infrastructure Expansion**

**Learning Material**:
- **Primary**: VMware Networking Documentation
  - **Where to find**: https://docs.vmware.com/en/VMware-Workstation-Pro/17.0/com.vmware.ws.using.doc/GUID-D9B0A52D-38A2-45D7-A9EB-987ACE77F93C.html
- **Supplementary**: Linode's Guide to Linux System Administration
  - **Where to find**: https://www.linode.com/docs/guides/linux-system-administration-basics/
- **Video Tutorial**: LearnLinuxTV VMware Networking Series
  - **Where to find**: https://www.youtube.com/c/LearnLinuxtv

**Lab Exercises**:
1. **Multi-VM Environment Setup**
   - Create a second Linux VM with a different distribution (CentOS/RHEL)
   - Configure networking between VMs (NAT and host-only networks)
   - Set up SSH key-based authentication between VMs
   - Practice basic system administration tasks on both distributions

2. **System Configuration Comparison Lab**
   - Compare file locations between distributions
   - Note differences in package management
   - Understand init system differences
   - Document the differences for future reference

**Challenge Task**:
- Create a centralized management setup:
  1. Configure one VM as an "admin node"
  2. Set up passwordless SSH to the other VM
  3. Create scripts that can perform tasks on both systems
- **Additional Resource**: SSH Configuration Guide
  - **Where to find**: https://www.ssh.com/academy/ssh/config

**Sunday: Storage Management**

**Learning Material**:
- **Primary**: DigitalOcean Storage Management Guide
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-partition-and-format-storage-devices-in-linux
- **Supplementary**: Red Hat Storage Administration Guide
  - **Where to find**: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_storage_devices/index
- **Video Tutorial**: LearnLinuxTV Storage Management Series
  - **Where to find**: https://www.youtube.com/playlist?list=PLT98CRl2KxKHnlbYhtABg6cF50bYa8Ulo

**Lab Exercises**:
1. **Disk Partitioning Lab**
   - Add new virtual disks to your VM
   - Create partitions using fdisk and parted
   - Format partitions with different file systems (ext4, xfs)
   - Mount and configure persistent mounts (fstab)

2. **LVM Lab**:
   - Create physical volumes, volume groups, and logical volumes
   - Extend and reduce logical volumes
   - Move data between volumes
   - Create and restore LVM snapshots

**Challenge Task**:
- Design a storage solution for a hypothetical application:
  1. Plan the partition scheme
  2. Implement using LVM for flexibility
  3. Configure automated snapshots for backup
  4. Document your design decisions and commands used
- **Additional Resource**: Linux Storage Expert - Blog
  - **Where to find**: https://www.linuxstorage.org/

## Week 2

### Monday (1-2 hours)
**Focus: LVM Basics**

**Learning Material**:
- **Primary**: DigitalOcean LVM Comprehensive Guide
  - **Where to find**: https://www.digitalocean.com/community/tutorials/an-introduction-to-lvm-concepts-terminology-and-operations
- **Supplementary**: Red Hat LVM Administrator's Guide
  - **Where to find**: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_logical_volumes/index
- **Interactive Tutorial**: TecMint LVM Tutorial with Examples
  - **Where to find**: https://www.tecmint.com/create-lvm-storage-in-linux/

**Lab Exercises**:
1. **LVM Creation Lab**
   - Add additional virtual disks to your VM
   - Create physical volumes (PVs) on the new disks
   - Create a volume group (VG) spanning multiple PVs
   - Create logical volumes (LVs) with different sizes and purposes
   - Create filesystems on LVs and mount them

2. **LVM Operations Lab**
   - Extend a logical volume while it's mounted
   - Reduce a logical volume (after unmounting)
   - Move data between physical volumes
   - Monitor LVM status with lvs, vgs, and pvs commands

**Challenge Task**:
- Simulate storage expansion scenario:
  1. Create an LV for a "database"
  2. Fill it to near capacity with dummy data
  3. Expand the storage without service interruption
  4. Document the steps and commands used
- **Additional Resource**: Linux Foundation Storage Administration Course Preview
  - **Where to find**: https://training.linuxfoundation.org/training/linux-storage-fundamentals/

### Tuesday (1-2 hours)
**Focus: Introduction to systemd**

**Learning Material**:
- **Primary**: DigitalOcean systemd Introduction
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units
- **Supplementary**: Arch Linux systemd Documentation
  - **Where to find**: https://wiki.archlinux.org/title/systemd
- **Reference**: systemd Official Manual Pages
  - **Where to find**: https://www.freedesktop.org/software/systemd/man/

**Lab Exercises**:
1. **systemd Basics Lab**
   - Examine the systemd unit hierarchy
   - Practice starting, stopping, enabling, and disabling services
   - Use journalctl to view logs for specific services
   - Understand target units and system states
   - Check service dependencies

2. **Service Troubleshooting Lab**
   - Intentionally break a service configuration
   - Use systemd tools to diagnose the issue
   - Fix the service and verify functionality
   - Check service resource usage with systemd-cgtop

**Challenge Task**:
- Analyze your system's boot process:
  1. Use systemd-analyze to check boot time
  2. Identify slow services with systemd-analyze blame
  3. Create a report on potential optimizations
- **Additional Resource**: Ubuntu Manpage for systemd-analyze
  - **Where to find**: https://manpages.ubuntu.com/manpages/focal/man1/systemd-analyze.1.html

### Wednesday (1-2 hours)
**Focus: Creating Custom systemd Services**

**Learning Material**:
- **Primary**: DigitalOcean systemd Services Creation Guide
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-create-a-systemd-service-in-linux
- **Supplementary**: Fedora systemd Service Examples
  - **Where to find**: https://fedoramagazine.org/systemd-service-unit-for-developer/
- **Reference**: systemd.service Manual Page
  - **Where to find**: https://www.freedesktop.org/software/systemd/man/systemd.service.html

**Lab Exercises**:
1. **Basic Service Creation Lab**
   - Write a simple shell script that outputs to a log file
   - Create a systemd service unit for this script
   - Configure service dependencies and ordering
   - Test service start, stop, enable, and status
   - View service logs with journalctl

2. **Advanced Service Configuration Lab**
   - Create a service with environment variables
   - Configure resource limits for your service
   - Set up service restart policies
   - Create a timer unit to run your service periodically
   - Test failure scenarios and recovery

**Challenge Task**:
- Design a web monitoring service:
  1. Create a script that checks website availability
  2. Configure it as a systemd service with appropriate restart policies
  3. Add a timer to run checks every 5 minutes
  4. Configure logging and reporting
- **Additional Resource**: Ubuntu Manpages for systemd.service and systemd.timer
  - **Where to find**: https://manpages.ubuntu.com/manpages/focal/man5/systemd.service.5.html and https://manpages.ubuntu.com/manpages/focal/man5/systemd.timer.5.html

### Thursday (1-2 hours)
**Focus: Advanced Package Management**

**Learning Material**:
- **Primary**: Ubuntu Package Management Guide
  - **Where to find**: https://ubuntu.com/server/docs/package-management
- **Supplementary**: Fedora/RHEL dnf Guide
  - **Where to find**: https://docs.fedoraproject.org/en-US/quick-docs/dnf/
- **Reference**: Debian APT Handbook
  - **Where to find**: https://www.debian.org/doc/manuals/debian-handbook/apt.en.html

**Lab Exercises**:
1. **Repository Management Lab**
   - Add and remove package repositories
   - Set up repository priorities
   - Create a local package repository
   - Configure apt preferences
   - Pin specific package versions

2. **Package Troubleshooting Lab**
   - Resolve broken dependencies
   - Fix interrupted installations
   - Use apt/dpkg to verify package integrity
   - Reinstall corrupted packages
   - Hold packages at specific versions

**Challenge Task**:
- Create a system preparation script:
  1. Write a script to install a predefined set of packages
  2. Include error handling for dependency issues
  3. Add repository management if needed
  4. Make it idempotent (can run multiple times safely)
- **Additional Resource**: Ubuntu Server Documentation on Package Management
  - **Where to find**: https://ubuntu.com/server/docs/package-management

### Friday (1-2 hours)
**Focus: Basic Shell Scripting**

**Learning Material**:
- **Primary**: Bash Guide for Beginners (TLDP)
  - **Where to find**: https://tldp.org/LDP/Bash-Beginners-Guide/html/
- **Supplementary**: Ryan's Bash Scripting Tutorial
  - **Where to find**: https://ryanstutorials.net/bash-scripting-tutorial/
- **Interactive Learning**: ShellCheck - Script Analysis Tool
  - **Where to find**: https://www.shellcheck.net/

**Lab Exercises**:
1. **Script Building Lab**
   - Write scripts of increasing complexity:
     - Simple file backup script
     - System information gathering script
     - Log parsing and analysis script
   - Use variables, conditionals, and loops
   - Implement proper error handling

2. **Script Automation Lab**
   - Set up cron jobs to run your scripts
   - Configure script logging
   - Create a script that emails reports
   - Implement simple user interaction in scripts

**Challenge Task**:
- Create a comprehensive system maintenance script:
  1. Updates system packages
  2. Cleans up temporary files
  3. Backs up important configuration files
  4. Checks disk usage and alerts if over threshold
  5. Logs all activities with timestamps
- **Additional Resource**: Advanced Bash-Scripting Guide
  - **Where to find**: https://tldp.org/LDP/abs/html/

### Weekend (6-8 hours total)

**Saturday: SSH Configuration and Security**

**Learning Material**:
- **Primary**: DigitalOcean SSH Essentials Guide
  - **Where to find**: https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys
- **Supplementary**: Mozilla Security SSH Guidelines
  - **Where to find**: https://infosec.mozilla.org/guidelines/openssh
- **Reference**: OpenSSH Manual Pages
  - **Where to find**: https://www.openssh.com/manual.html

**Lab Exercises**:
1. **SSH Setup and Hardening Lab**
   - Configure SSH with key-based authentication
   - Disable password authentication
   - Change default SSH port
   - Implement fail2ban for brute force protection
   - Configure SSH client configuration file

2. **Advanced SSH Features Lab**
   - Set up SSH agent forwarding
   - Configure SSH tunnels and port forwarding
   - Use SSH for secure file transfers (scp/sftp)
   - Create SSH jump hosts
   - Practice with SSH config file for multiple hosts

**Challenge Task**:
- Build a secure remote access solution:
  1. Configure a bastion host setup between your VMs
  2. Implement certificate-based authentication
  3. Set up logging and monitoring for SSH connections
  4. Document your security measures and their purposes
- **Additional Resource**: SSH.com Academy Resources
  - **Where to find**: https://www.ssh.com/academy/ssh/protocol

**Sunday: Review and Challenge Labs**

**Learning Material**:
- **Primary**: Linux Command Line Cheat Sheet by Dave Child
  - **Where to find**: https://cheatography.com/davechild/cheat-sheets/linux-command-line/
- **Supplementary**: TryHackMe Linux Stronghold Room
  - **Where to find**: https://tryhackme.com/room/linuxstrengthtraining
- **Reference**: Linux Foundation Tutorials
  - **Where to find**: https://www.linuxfoundation.org/resources/publications/tutorials

**Lab Exercises**:
1. **Comprehensive Review Lab**
   - Work through a series of tasks that incorporate all week 1-2 skills:
     - User and permission management
     - File system operations
     - Package installation and configuration
     - Service management
     - Basic shell scripting

2. **OverTheWire: Bandit Labs**
   - Complete OverTheWire Bandit challenges (levels 1-10)
   - These are pre-configured Linux puzzles that test your command line skills
   - Each level presents a unique challenge to find passwords for the next level
   - Document the commands and concepts used for each level
   - Create a personal "lessons learned" document

**Challenge Task**:
- Complete OverTheWire: Bandit challenges (levels 1-10)
  - **Where to find**: https://overthewire.org/wargames/bandit/
  - Document the commands and concepts used for each level
  - Create a personal "lessons learned" document
- **Additional Resource**: Ubuntu's Official Command Line Tutorial
  - **Where to find**: https://ubuntu.com/tutorials/command-line-for-beginners

## Week 1-2 Learning Progress Checklist

### File System Management
- [ ] Navigate directories and locate files using find and grep with advanced options
- [ ] Use text processing tools (awk, sed) to manipulate file content
- [ ] Create and extract archives with various compression methods
- [ ] Analyze disk usage with appropriate tools
- [ ] Write shell scripts to automate file operations

### User and Permission Management
- [ ] Create and manage users with specific requirements
- [ ] Configure and use groups effectively for access control
- [ ] Set complex file permissions using both symbolic and numeric notation
- [ ] Implement and test Access Control Lists (ACLs)
- [ ] Configure sudo access with appropriate restrictions

### Storage Management
- [ ] Create, format, and mount partitions with different file systems
- [ ] Configure persistent mounts using /etc/fstab
- [ ] Set up and manage Logical Volume Management (LVM)
- [ ] Expand and reduce volumes as needed
- [ ] Implement storage snapshots for backup purposes

### System Services
- [ ] Manage services using systemd commands (start, stop, enable, disable)
- [ ] Analyze service logs with journalctl
- [ ] Create custom systemd service units
- [ ] Configure service dependencies and ordering
- [ ] Set up timer units for scheduled execution

### Package Management
- [ ] Perform basic package operations (install, remove, update)
- [ ] Manage package repositories and priorities
- [ ] Handle package dependencies and conflicts
- [ ] Lock packages at specific versions
- [ ] Compare package management across different distributions

### Shell Scripting
- [ ] Write maintainable shell scripts with proper error handling
- [ ] Use variables, conditionals, and loops effectively
- [ ] Set up scheduled tasks with cron
- [ ] Implement logging in scripts
- [ ] Create system maintenance automation scripts

### SSH and Remote Management
- [ ] Configure SSH with key-based authentication
- [ ] Implement SSH security best practices
- [ ] Use SSH for remote file transfers
- [ ] Set up SSH tunnels and port forwarding
- [ ] Configure complex SSH client options

### Lab Environment
- [ ] Set up and manage multiple Linux VMs
- [ ] Configure networking between VMs
- [ ] Document system configurations
- [ ] Create and restore system snapshots
- [ ] Build a complete lab environment for future learning modules
