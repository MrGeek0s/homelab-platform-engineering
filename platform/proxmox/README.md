# Platform & Virtualization — Proxmox VE

## Purpose
This section documents the virtualization platform used as the foundation of the lab.
The goal is to simulate **production-style platform engineering** under **realistic constraints**, not to optimize for high availability or cloud elasticity.

## Platform Overview
- Hypervisor: Proxmox VE
- Topology: Single-node cluster
- Virtualization: KVM/QEMU
- Networking: Linux bridges with VLAN tagging
- Storage: Local storage (no shared storage)

## Design Philosophy
- Intentional resource constraints
- Clear separation of responsibilities per VM
- Platform stability prioritized over workload convenience
- Observability and security treated as core platform requirements

## Why Single Node
This platform intentionally uses a single node to:
- Force proper capacity planning
- Expose real failure modes
- Avoid masking design issues with redundancy
- Reflect small on-prem and edge deployments

## Scope
This section covers:
- Platform architecture
- VM role separation
- Resource allocation strategy
- Constraints and trade-offs

Downstream sections (networking, security, observability, identity) build on this foundation.
