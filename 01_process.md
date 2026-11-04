# 01. Processes and Address Spaces

## What is a process?
A **process** is a program in execution. A program is a passive file; a process includes its running state and resources.

## Typical process address space
- **Text:** executable instructions (often read-only).
- **Data:** initialized global and static variables.
- **BSS:** zero-initialized or uninitialized global and static variables.
- **Heap:** dynamically allocated memory.
- **Stack:** function call frames and local variables.

## Process state
A simplified model is **New → Ready → Running → Waiting/Blocked → Ready → Terminated**. A running process may return to Ready when preempted.

## fork() and exec()
- `fork()` creates a child process, initially with a logically separate address space.
- An `exec`-family call replaces the calling process's program image; it does not create another process.

**Review:** Why can two processes use the same virtual address without sharing the same physical memory?
