# Platform Constraints & Trade-Offs

## Intentional Constraints
The following constraints are deliberately accepted:

- Single Proxmox node
- No high availability
- No live migration
- No shared storage
- Finite CPU, memory, and disk

## Why These Constraints Exist
- Reflect real-world limitations
- Prevent overengineering
- Force prioritization
- Make failure modes visible

## Trade-Off Analysis

| Decision | Benefit | Cost |
|--------|--------|------|
| Single node | Simplicity, realism | No redundancy |
| No HA | Clear failure visibility | Downtime |
| Local storage | Predictable behavior | No migration |
| Strict VM roles | Security, clarity | More VMs |

## Operational Impact
- Observability becomes mandatory
- Resource planning becomes critical
- Changes are evaluated carefully
- Failures become learning events

This environment prioritizes **understanding systems behavior** over theoretical perfection.
