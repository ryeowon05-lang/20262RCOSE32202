# 03. Mode Switches and Context Switches

## Mode switch
A **mode switch** changes CPU privilege level (for example, user mode to kernel mode). It does not necessarily change the running process.

## Context switch
A **context switch** changes which thread or process executes. The OS saves the old execution context and restores the next one.

## Important distinction
- A system call can cause a mode switch and return to the same process.
- A timer interrupt can trigger a scheduling decision and a context switch.
- Context switching has overhead from saving/restoring state and possible cache/TLB effects.

## Timer interrupt and time slice
A periodic timer gives the kernel opportunities to regain control. A **time slice** is how long a task may run before preemption under a particular scheduling policy; it is not necessarily equal to one timer period.

**Review:** Does every interrupt cause a context switch? No: the kernel may resume the interrupted task.
