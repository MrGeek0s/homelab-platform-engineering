# Virtual Machine Roles & Separation

## Design Principle
Each virtual machine has **one clear responsibility**.
No VM is allowed to perform multiple infrastructure roles.

This follows the principle of **least responsibility**.

## VM Role Overview

| VM Role        | Responsibility                              | Reason for Isolation |
|----------------|---------------------------------------------|----------------------|
| Firewall       | Routing, firewall, VPN termination           | Security boundary    |
| Monitoring     | Metrics, logs, alerting                      | Operational visibility |
| Identity       | Authentication, authorization, DNS           | Critical dependency  |
| Bastion        | Administrative access                       | Access control       |
| Automation     | Workflow orchestration                       | Workload isolation  |
| DMZ            | External ingress (tunnels)                   | Reduced blast radius |

## Why Role Separation Matters
- Limits blast radius
- Simplifies troubleshooting
- Improves auditability
- Prevents privilege escalation across services

This model mirrors how production platforms isolate control-plane components.
