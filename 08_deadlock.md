# 08. Deadlocks

## Definition
A **deadlock** is a situation where a set of processes or threads cannot proceed because each is waiting for resources or events dependent on the others.

## Four necessary conditions (Coffman conditions)
1. **Mutual exclusion** for at least one resource.
2. **Hold and wait:** holding resources while requesting more.
3. **No preemption:** resources cannot simply be taken away.
4. **Circular wait:** a cycle of resource dependencies.

## Strategies
- **Prevention:** structurally break at least one necessary condition.
- **Avoidance:** allocate only when the system remains in a safe state.
- **Detection and recovery:** detect deadlocks and then recover.

## Example
Thread A holds lock X and waits for Y; thread B holds Y and waits for X. A consistent lock acquisition order can prevent this cycle.

**Review:** Why does imposing a global lock order prevent circular wait?
