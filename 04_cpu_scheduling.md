# 04. CPU Scheduling

## Why scheduling matters
When multiple runnable tasks compete for a CPU, the scheduler chooses which runs next.

## Common goals
- **Throughput:** completed jobs per unit time.
- **Turnaround time:** completion time minus arrival time.
- **Waiting time:** time spent in the ready queue.
- **Response time:** first run time minus arrival time.
- **Fairness:** avoiding unreasonable starvation.

## Common policies
- **FCFS:** first come, first served; simple but can suffer convoy effects.
- **SJF:** shortest job first; minimizes average waiting time under ideal assumptions with known burst lengths.
- **Round Robin:** each runnable task gets a time quantum, then rotates.
- **Priority scheduling:** runs higher-priority tasks first; aging can reduce starvation.

## Trade-off
A tiny time quantum improves responsiveness but increases context-switch overhead. A very large quantum behaves more like FCFS.

**Review:** Why might a scheduler optimize response time for interactive workloads rather than only throughput?
