# 10. Operating Systems Review

## Quick comparison table
| Concept | Key idea |
|---|---|
| Program vs. process | Static executable vs. running instance |
| API vs. system call | Programming interface vs. kernel service entry |
| Mode switch vs. context switch | Privilege change vs. running-task change |
| Ready vs. blocked | Runnable but waiting for CPU vs. waiting for an event |
| Pipe vs. shared memory | Byte-stream IPC vs. mapped shared region |
| Virtual vs. physical address | Program-visible address vs. actual memory location |
| Mutex vs. semaphore | Mutual exclusion vs. count-based coordination |
| Deadlock vs. starvation | Circular inability to proceed vs. indefinite lack of progress |

## Self-test
1. Does `exec()` create a new PID? **No; it replaces the current process image.**
2. Does every API call trigger a system call? **No.**
3. Does every timer interrupt force a different process to run? **No.**
4. Can two processes use the same virtual address? **Yes.**
5. Does `mq_receive()` write into the receiver's supplied buffer? **Yes.**
6. Is a large time quantum always better? **No; it trades responsiveness for lower switching overhead.**
7. Does a TLB miss always mean a page fault? **No.**
8. Can a race condition occur on a single-core CPU? **Yes, through interleaving.**
9. Can consistent lock ordering prevent circular wait? **Yes.**
10. Does `write()` guarantee durable storage immediately? **Not necessarily.**

## Next steps
Revise these notes after lectures and add small, original examples. Never upload restricted course project source code.
