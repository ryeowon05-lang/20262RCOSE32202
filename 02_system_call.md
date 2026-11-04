# 02. System Calls and Privilege Modes

## User mode vs. kernel mode
User mode restricts privileged operations. Kernel mode permits the OS to manage hardware and protected resources.

## System call
A **system call** is a controlled entry from user space into the kernel to request an OS service, such as file I/O or process management.

Typical path:
1. A program calls a library wrapper or invokes a system-call interface.
2. The CPU enters the kernel through a defined mechanism.
3. The kernel checks arguments and performs the operation.
4. Control returns to user mode.

## API is not the same as a system call
An **API** describes a programming interface. Not every API call enters the kernel: `sprintf()` usually formats a string entirely in user space.

**Review:** Why is it incorrect to say that every C library function causes a mode switch?
