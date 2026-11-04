# 07. Synchronization

## Race condition
A **race condition** occurs when the result depends on the timing or interleaving of concurrent operations.

## Critical section
A section of code accessing shared mutable state that must be protected against unsafe concurrent access.

## Tools
- **Mutex:** provides mutual exclusion to a critical section.
- **Semaphore:** maintains a count and supports wait/signal-style coordination.
- **Condition variable:** lets threads wait for a condition while coordinating with a mutex.
- **Atomic operations:** indivisible operations useful for counters and synchronization primitives.

## Example
If two threads both read `counter = 0`, increment locally, and write `1`, the final result can be `1` rather than `2`.

**Review:** Why is `counter++` not automatically thread-safe?
