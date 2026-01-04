# Platform Architecture

## High-Level Architecture
The platform is built on a single Proxmox VE node acting as the authoritative control plane for:
- Compute
- Networking
- Storage
- Virtual machine lifecycle

All infrastructure services are deployed as isolated virtual machines.

## Architecture Characteristics
- No container workloads on the hypervisor
- No multi-purpose VMs
- No shared admin access across services
- Centralized management via Proxmox only

## Control Plane Responsibilities
The Proxmox node is responsible for:
- VM scheduling and lifecycle
- Virtual networking (bridges, VLANs)
- Resource enforcement
- Platform observability (indirectly)

Application and infrastructure services never run directly on the host.

## Failure Model
- Single-node failure impacts all services
- No HA or live migration
- Failures are intentional learning scenarios

This architecture mirrors:
- Budget-constrained on-prem environments
- Edge or branch deployments
- Early-stage production platforms
