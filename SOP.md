# Standard Operating Procedure  
**Toaplance World**  
**Accra, Ghana**  
📞 +233-555-123-456  

---

## Reversion Info  
**Version:** 1.0  
**Date:** July 18, 2025  
**Created By:** Abiba Musah  
**Document Status:** Active  

---

## ✅ Approval Table

| Version | Date       | Name         | Role       |
|---------|------------|--------------|------------|
| 1.0     | 2025-07-18 | Abiba Musah  | Creator    |
| 1.1     | 2025-07-18 | Ali Abdaal   | Reviewer   |
| 1.2     | 2025-07-18 | Jay Shetty   | Approver   |

---

## Purpose  
The goal of this SOP is to define a repeatable process for setting up a virtual Linux server for testing web applications at Toaplance World. With this SOP, our team ensures all server setups are standardized, secure, and aligned with our internal infrastructure needs.

---

## Scope & Objectives  
This SOP applies to all Toaplance World team members responsible for IT infrastructure, particularly in development and QA environments. It is intended for internal web app testing scenarios and can be adapted for larger-scale deployments.

### Objectives:
- Provision a virtual Linux server for web testing  
- Install all required software packages securely  
- Ensure the system follows company compliance and documentation guidelines  
- Provide clear responsibility mapping for team coordination

---

## Accountability Matrix  

| Task                            | Responsible     | Backup Contact       | Reviewer      |
|---------------------------------|------------------|-----------------------|----------------|
| Define server specs             | Abiba Musah      | Jay Shetty            | Ali Abdaal      |
| Create virtual machine          | Ali Abdaal       | Abiba Musah           | Jay Shetty      |
| Install Linux + web tools       | Abiba Musah      | Ali Abdaal            | Jay Shetty      |
| Perform system tests            | Ali Abdaal       | Jay Shetty            | Abiba Musah     |
| Document system details         | Abiba Musah      | Ali Abdaal            | Jay Shetty      |

---

## Definitions  
- **SOP**: Standard Operating Procedure  
- **VM**: Virtual Machine  
- **QA**: Quality Assurance  
- **ISO**: Installation image for OS setup  
- **LAMP**: Linux, Apache, MySQL/MariaDB, PHP stack  

---

## Procedure Steps  

### Step 1: Define Requirements  
- Determine the purpose of the VM (e.g., testing a new login feature).  
- Choose a lightweight Linux distribution (Ubuntu Server 22.04 LTS is recommended).  
- Specify minimum specs: 2 vCPUs, 2GB RAM, 20GB storage.  
- Confirm network access and firewall rules with the sysadmin team.

### Step 2: Create the Virtual Machine  
- Use VirtualBox, VMware, or Proxmox (depending on your setup).  
- Set the VM name and assign it to the QA group.  
- Attach the downloaded Linux ISO.  
- Enable NAT or Bridged networking for internet access.  

### Step 3: Install the Operating System  
- Boot the VM and start the Ubuntu Server installation.  
- Set hostname (e.g., `webtest-toaplance`) and timezone (Africa/Accra).  
- Create a non-root user (e.g., `tester`).  
- Apply system updates using `sudo apt update && sudo apt upgrade`.

### Step 4: Install Required Software  
- Install Apache: `sudo apt install apache2`  
- Install PHP: `sudo apt install php libapache2-mod-php`  
- Install MySQL: `sudo apt install mysql-server`  
- Enable services: `sudo systemctl enable apache2 mysql`  
- Place test web app files in `/var/www/html`  

### Step 5: Verify and Harden System  
- Test web server access using the server's IP in a browser.  
- Verify PHP info with a test `info.php` page.  
- Change default passwords and disable root login via SSH.  
- Create a system snapshot if your platform supports it.

### Step 6: Documentation and Handover  
- Record key info:  
  - Hostname  
  - IP address  
  - OS version  
  - Installed software  
  - Assigned tester  
- Save this data in a shared team drive or config tracker.  
- Notify the team via email or Slack with access credentials

---

## 📄 Reference or Related Documents  
- `ubuntu-server-setup-guide.md` – Basic OS installation steps  
- `lamp-stack-checklist.pdf` – Minimum requirements for web testing  
- `webapp-test-report-template.docx` – QA reporting format  

