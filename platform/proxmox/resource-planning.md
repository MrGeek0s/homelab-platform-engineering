# Resource Planning & Allocation Strategy

## Guiding Principles
- Allocate resources based on **service criticality**
- Avoid over-provisioning
- Accept and observe resource pressure
- Scale only when justified by metrics

## Memory Allocation Strategy
- Monitoring services receive higher memory due to:
  - Time-series databases
  - Log ingestion
  - Query workloads
- Firewall resources are stable and predictable
- Identity services are isolated with moderate allocation
- Bastion and DMZ are intentionally lightweight

## Disk Allocation Strategy
- Monitoring VM allocated larger disk for:
  - Metrics retention
  - Log storage
- Identity and automation receive moderate disk
- Bastion and DMZ use minimal persistent storage

## CPU Allocation
- No CPU overcommit tuning
- Default scheduler behavior observed
- Performance issues analyzed via observability, not assumptions

## Outcome
This strategy exposes:
- Memory pressure behavior
- Disk growth patterns
- Impact of poor sizing decisions

These signals are used to guide future improvements.
