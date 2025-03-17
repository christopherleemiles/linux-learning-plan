# Weeks 1-2: Detailed Daily Plan for Linux System Administration Fundamentals

## Week 1

### Monday (1-2 hours)
**Focus: File System Management Basics**
- **Resource**: Linux Journey - "Grasshopper" section on file system
  - **Where to find**: https://linuxjourney.com/lesson/filesystem-hierarchy
- **Practice**: 
  - Navigate and create complex directory structures
  - Use find and grep to locate specific files
  - Practice basic file system commands (ls, cp, mv, etc. with advanced options)
- **Goal**: Become comfortable with everyday file system operations

### Tuesday (1-2 hours)
**Focus: Advanced File Operations**
- **Resource**: A Cloud Guru - Linux Command Line tutorial
  - **Where to find**: https://acloudguru.com/course/the-system-administrators-guide-to-bash-scripting (free trial available)
  - **Alternative**: https://www.digitalocean.com/community/tutorials/linux-commands-every-developer-should-know (free)
- **Practice**:
  - Use du, df, and ncdu to analyze disk usage
  - Practice with awk and sed for text processing
  - Create archive files (tar, gzip, etc.)
- **Goal**: Handle complex file operations efficiently

### Wednesday (1-2 hours)
**Focus: User and Group Management**
- **Resource**: TryHackMe - Linux Fundamentals Part 2
  - **Where to find**: https://tryhackme.com/room/linuxfundamentalspart2 (free account required)
- **Practice**:
  - Create users with specific home directories
  - Assign users to groups
  - Set up basic sudo access
- **Goal**: Manage system users and basic permissions

### Thursday (1-2 hours)
**Focus: File Permissions**
- **Resource**: Linux Journey - "Permissions" section
  - **Where to find**: https://linuxjourney.com/lesson/file-permissions
- **Practice**:
  - Set complex permissions with chmod
  - Change ownership with chown
  - Implement basic ACLs
- **Goal**: Control file access securely

### Friday (1-2 hours)
**Focus: Basic Package Management**
- **Resource**: DigitalOcean tutorials on apt and dpkg
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-manage-packages-in-ubuntu-and-debian-with-apt-get-apt-cache
- **Practice**:
  - Install, update, and remove packages
  - Hold package versions
  - Find package information
- **Goal**: Manage software effectively

### Saturday (3-4 hours)
**Focus: Home Lab Setup**
- **Resource**: VMware Workstation documentation
  - **Where to find**: https://docs.vmware.com/en/VMware-Workstation-Pro/
  - **Alternative**: YouTube tutorial - "How to Install Ubuntu Server on VMware Workstation" by LearnLinuxTV
    - https://www.youtube.com/watch?v=HmehDKO5xyI
- **Practice**:
  - Set up two VMs: Ubuntu Server and CentOS/RHEL
  - Configure networking between VMs (using VMware's NAT and Host-only options)
  - Set up SSH access between machines
- **Goal**: Create a lab environment for future practice

### Sunday (3-4 hours)
**Focus: Basic Storage Management**
- **Resource**: "How Linux Works" Chapter 4 (Disks and Filesystems)
  - **Where to find**: Book by Brian Ward (No Starch Press)
  - **Alternative**: DigitalOcean tutorial on disk management
    - https://www.digitalocean.com/community/tutorials/how-to-partition-and-format-storage-devices-in-linux
- **Practice**:
  - Create partitions with fdisk/parted
  - Format partitions with different file systems
  - Mount and unmount file systems
- **Goal**: Handle basic storage operations

## Week 2

### Monday (1-2 hours)
**Focus: LVM Basics**
- **Resource**: DigitalOcean LVM tutorial
  - **Where to find**: https://www.digitalocean.com/community/tutorials/an-introduction-to-lvm-concepts-terminology-and-operations
- **Practice**:
  - Create a physical volume, volume group, and logical volume
  - Extend a logical volume
  - Create a basic filesystem on LVM
- **Goal**: Understand LVM concepts

### Tuesday (1-2 hours)
**Focus: Introduction to systemd**
- **Resource**: DigitalOcean systemd introduction
  - **Where to find**: https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units
- **Practice**:
  - Start, stop, and check status of services
  - Enable/disable services
  - View service logs with journalctl
- **Goal**: Understand service management basics

### Wednesday (1-2 hours)
**Focus: Creating Basic systemd Services**
- **Resource**: Linux Academy "Creating systemd Services" 
  - **Where to find**: Now part of A Cloud Guru - free trial available
  - **Alternative**: DigitalOcean tutorial on creating systemd services
    - https://www.digitalocean.com/community/tutorials/how-to-create-a-systemd-service-in-linux
- **Practice**:
  - Write a simple service file
  - Test service start/stop
  - Configure basic service options
- **Goal**: Create custom services

### Thursday (1-2 hours)
**Focus: Advanced Package Management**
- **Resource**: "Linux Bible" chapter on package management
  - **Where to find**: Book by Christopher Negus (Wiley)
  - **Alternative**: FOSS Linux article on package management
    - https://www.fosslinux.com/24395/debian-vs-rpm-package-management-systems.htm
- **Practice**:
  - Compare apt (Ubuntu) and dnf/yum (CentOS)
  - Handle dependencies
  - Search for specific packages
- **Goal**: Master package management across distros

### Friday (1-2 hours)
**Focus: Basic Shell Scripting**
- **Resource**: Linux Journey - "Grasshopper" shell scripting section
  - **Where to find**: https://linuxjourney.com/lesson/shell-scripting
- **Practice**:
  - Write a simple backup script
  - Create a user management script
  - Set up script scheduling with cron
- **Goal**: Automate basic tasks

### Saturday (3-4 hours)
**Focus: SSH Configuration and Security**
- **Resource**: DigitalOcean SSH essentials tutorial
  - **Where to find**: https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys
- **Practice**:
  - Set up key-based authentication
  - Configure SSH hardening options
  - Set up a basic SSH config file
- **Goal**: Secure remote access

### Sunday (3-4 hours)
**Focus: Review and Challenge Lab**
- **Resource**: OverTheWire: Bandit (levels 1-10)
  - **Where to find**: https://overthewire.org/wargames/bandit/
- **Practice**:
  - Complete a series of challenges that test all skills learned
  - Create a summary document of commands learned
  - Review your progress against the learning checklist
- **Goal**: Solidify all week 1-2 learning

## Week 1-2 Learning Progress Checklist

- [ ] Navigate and manage files effectively with command line tools
- [ ] Create and manage users and groups with appropriate permissions
- [ ] Manage packages using apt and yum/dnf
- [ ] Create basic partitions and filesystems
- [ ] Create and manage basic LVM volumes
- [ ] Start, stop, and configure systemd services
- [ ] View logs with journalctl
- [ ] Write simple shell scripts for automation
- [ ] Configure secure SSH with key-based authentication
- [ ] Set up a functioning multi-VM lab environment
