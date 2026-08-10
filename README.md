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




## Current Infrastructure
**Router (OpenWRT)**

The router serves as the core networking device for the homelab.

Current configuration includes:

- Multiple wireless networks
  - Main Network
  - Guest Network
  - IoT Network
- VLAN Segmentation
  - Management VLAN
  - Server VLAN
  - IoT VLAN
- Firewall Rules
  - Server access restrictions
  - Guest network isolation
  - IoT network isolation
  - Inter-VLAN communication where required

Future improvements include forwarding all DNS traffic through Pi-hole for network-wide filtering.

**Managed Switch**

The managed switch extends the VLAN architecture throughout the lab.

Configuration includes:
- Tagged and untagged VLAN ports
- Port VLAN IDs (PVIDs)
- Dedicated management VLAN
- 100 Mbps bandwidth limitation for IoT devices
- Port exclusions where appropriate

**Raspberry Pi 5**

The Raspberry Pi functions as a lightweight infrastructure server.

Current services include:

- Pi-hole
- Flask API
- Tailscale
- Uptime Kuma
- Prometheus & Grafana Monitoring
- Future utility services

**Proxmox Node 1 (PowerSpec G315)**

Primary compute server.

Primary responsibilities:

- AI experimentation
- GPU passthrough
- High-resource virtual machines
- Infrastructure testing

**Proxmox Node 2 (Dell OptiPlex)**

Secondary virtualization node optimized for lightweight workloads.

Current and planned workloads:

- Docker
- n8n
- PostgreSQL
- Directus
- Caddy
- Linux VMs
- Windows Server VMs
- LXC containers


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



## Documentation

This repository contains documentation for the overall infrastructure design.

Additional documentation maintained outside of this README includes:

- Network topology
- VLAN design
- IP addressing
- Firewall rules
- Service deployments
- Docker Compose configurations
- Infrastructure notes
- Troubleshooting documentation

## Security

Security is a major design consideration throughout the lab.

Current implementations include:

- VLAN segmentation
- OpenWRT firewall rules
- Tailscale zero-trust networking
- Cloudflare Tunnel for externally accessible services
- SSH authentication
- Docker network isolation
- Principle of least privilege for service access

## Current Projects Hosted

- Docker infrastructure
- n8n automation
- PostgreSQL databases
- Directus administration platform
- Flask API services
- Pi-hole DNS filtering
- Uptime Kuma monitoring
- Local AI experimentation

## What I Learned

This project has provided practical experience in:

- Linux Administration
- Enterprise Networking
- VLAN Design
- Firewall Configuration
- Docker
- Proxmox
- Virtualization
- Infrastructure Planning
- Network Security
- System Troubleshooting
- Service Deployment
- Infrastructure Documentation

## Challenges

Some of the larger challenges included:

- Designing VLAN segmentation
- Creating secure firewall policies
- Planning infrastructure growth
- Inter-VLAN routing
- Hardware resource allocation
- Container networking
- Remote administration
- Building a maintainable infrastructure

## Roadmap

Short-Term
- Configure Pi-hole as network-wide DNS
- Complete Docker migration
- Improve monitoring

Medium-Term
- Build a Proxmox cluster
- Deploy NAS storage
- Add centralized logging
- Implement automated backups

Long-Term
- Kubernetes
- Infrastructure as Code (Terraform / Ansible)
- High Availability
- Local AI infrastructure
- GitOps workflows


