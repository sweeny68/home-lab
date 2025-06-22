# Home Pentesting Lab Infrastructure

This repository documents my self-hosted pentesting lab environment, designed to support hands-on security testing, learning, and certification preparation (e.g., Security+).

---

## Environment Overview

- **Host:** Dell OptiPlex 3050 running Ubuntu Server 22.04 LTS  
- **Virtualization:** KVM/QEMU managed via Cockpit  
- **Networking:** Tailscale VPN for secure remote access, no port forwarding  
- **VMs:**  
  - Kali Linux (ISO-based install)  
  - Metasploitable2 (VMDK image)  
  - Custom VulnHub VMs (OVA/ISO)  

---

## Key Features & Technical Highlights

- **VM Management:**  
  Leveraging Cockpit for streamlined VM lifecycle management, including starting, stopping, and resource allocation without CLI complexity.  

- **Storage:**  
  Utilized QCOW2 disk images for snapshot support and storage efficiency; converted VMDK files where necessary.  

- **Security:**  
  Isolated VM network segments within libvirt to minimize host exposure.  
  Access to the lab via Tailscale ensures encrypted, zero-trust remote connectivity.

- **Automation:**  
  Scripts maintained for VM image conversion and deployment (not included here for security).  

---

## Usage

- Access Cockpit web UI at `https://<host-ip>:9090` for VM control.  
- Connect to lab VMs via Tailscale IPs or local bridged network as configured.  

---

## Next Steps

- Expand VM catalog with additional vulnerable targets from VulnHub.  
- Integrate automated VM provisioning via Ansible.  
- Implement centralized logging and monitoring (ELK stack).  

---

## Contact

For technical questions or collaboration, reach out via LinkedIn: [linkedin.com/in/oranmcclintock](https://linkedin.com/in/oranmcclintock)

---

*This lab setup is a practical foundation supporting ongoing penetration testing skill development and sysadmin experience.*
