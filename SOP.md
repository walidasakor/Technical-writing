# Standard Operating Procedure  
**Toaplance World**  
**Accra, Ghana**  
Phone: +233-XXX-XXXX  

---

## Revision Info  
**Version:** 1.0  
**Date:** 2025-07-17  
**Created By:** Abiba Musah  

---

## Approval Table

| Version | Date       | Name         | Role      |
|---------|------------|--------------|-----------|
| 1.0     | 2025-07-17 | Abiba Musah  | Author    |
| 1.1     | 2025-07-17 | Ali Abdaal   | Reviewer  |
| 1.2     | 2025-07-17 | Jay Shetty   | Approver  |

---

## Purpose  
📌 This SOP outlines the standardized process for creating and managing virtual machines at Toaplance World to ensure consistent configuration, security, and resource management across all systems.

---

## Scope  
This document applies to all IT staff, system administrators, and cloud engineers at Toaplance World responsible for provisioning, configuring, and maintaining virtual machines (VMs) used for development, testing, or production.

### Objectives
- Standardize VM configurations  
- Ensure efficient resource use  
- Maintain thorough documentation  
- Enforce security best practices  

---

## Accountability Matrix

| Task                       | Responsible Person | Emergency Contact       | Reviewer/Approver       |
|----------------------------|--------------------|------------------------|------------------------|
| VM planning & requirements | Abiba Musah        | abiba@toaplance.com    | Jay Shetty             |
| VM creation & configuration| Ali Abdaal         | ali@toaplance.com      | Jay Shetty             |
| OS installation & updates  | Abiba Musah        | abiba@toaplance.com    | Jay Shetty             |
| Testing & validation       | Ali Abdaal         | ali@toaplance.com      | Jay Shetty             |
| Documentation & handover   | Abiba Musah        | abiba@toaplance.com    | Ali Abdaal             |

---

## Definitions  
- **VM**: Virtual Machine  
- **ISO**: Disk image used for OS installation  
- **Snapshot**: A saved VM state at a point in time  
- **vSphere**: VMware’s virtualization management platform  

---

## Procedure Steps

### Step 1: Planning  
- Identify VM purpose (e.g., web app testing, internal tools).  
- Define CPU, RAM, disk size, and networking needs.  
- Check host capacity and datastore availability.  
- Confirm OS version and licensing requirements.

### Step 2: VM Creation  
- Log in to vSphere with secure credentials.  
- Right-click the target host or cluster, select **New Virtual Machine**.  
- Choose **Custom Configuration**, assign VM name and resource pool.  
- Select datastore and compatibility level.  
- Allocate CPU, RAM, and disk resources.  
- Configure network adapter, assign to appropriate VLAN.

### Step 3: OS Installation  
- Mount the installation ISO media.  
- Boot VM from ISO and install the OS (set language, timezone, users).  
- Perform system updates and install tools like VMware Tools.

### Step 4: Testing and Hardening  
- Verify network connectivity internally and externally.  
- Confirm VM boots without errors.  
- Run functional tests as required.  
- Set strong passwords, enable firewall, disable unnecessary services.

### Step 5: Documentation and Transfer  
- Log VM details: hostname, IP address, OS version, assigned owner, and purpose.  
- Take a snapshot if applicable.  
- Share credentials securely with the responsible team.

---

## Reference or Related Documents  
- `vm-template-config.yaml` – VM configuration template  
- `security-hardening-guide.pdf` – IT security policy checklist  
- `network-vlan-map.xlsx` – VLAN assignment sheet  
