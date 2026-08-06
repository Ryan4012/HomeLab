## Home Infrastructure & Homelab
A self-hosted infrastructure lab built to explore virtualization, networking, automation, cloud technologies, and secure systems administration.

## Overview
This project is my personal homelab built to develop hands-on experience with enterprise infrastructure, virtualization, networking, automation, and self-hosted services.

Rather than relying solely on cloud providers, I wanted to build an environment where I could design, deploy, secure, and manage infrastructure from the ground up. The lab serves as a platform for experimenting with Linux systems, Docker containers, virtualization, networking, AI workloads, and production-inspired deployments.

As the project has evolved, the environment has grown from a single Proxmox server into a multi-device infrastructure consisting of dedicated virtualization hosts, containerized services, networking equipment, and management tools.

## Motivation and Goals
The primary goal of this project is to gain practical experience with technologies commonly used in systems administration, cloud engineering, DevOps, and infrastructure engineering.

**Areas of focus include:**

Linux administration
Virtualization with Proxmox
Containerized applications
Network segmentation
Infrastructure security
Self-hosted services
Automation
AI experimentation
High availability concepts

This homelab provides a safe environment to build, break, troubleshoot, and improve systems without affecting production environments.


## Infrastructure Overview
**Hardware**

|Device	                      |  Purpose                           |
|-----------------------------|------------------------------------|
|PowerSpec G315	              | Primary Proxmox compute node       |
|Dell OptiPlex 7050 Micro	    | Secondary Proxmox node             |
|Raspberry Pi 5	              | Network services and utility server|
|GL.iNet Router (OpenWRT)	    | Routing, firewall, VLAN management |
|Netgear Smart Managed Switch	| VLAN-aware switching               |


## Technology Stack
**Virtualization**
- Proxmox VE
- Virtual Machines
- LXC Containers
- Docker

**Operating Systems**
- Debian
- Ubuntu
- Kali Linux
- Linux From Scratch
- Windows Server

**Networking**
- OpenWRT
- VLANs
- Firewall Rules
- Pi-hole
- Tailscale
- Cloudflare Tunnel
- DNS
- DHCP

**Applications**
- n8n
- PostgreSQL
- Directus
- Caddy
- Uptime Kuma
- Flask
- Local AI Models (planned)


## Continue here

**Diagrams**
<table>
  <tr>
    <th>Architecture</th>
    <th>Network</th>
  </tr>
  <tr>
    <td><img src="./Diagrams/Architecture-Diagram.png" alt="Architecture Diagram" width="500" /></td>
    <td><img src="./Diagrams/Network-Diagram.png" alt="Network Diagram" width="500" /></td>
  </tr>
</table>




