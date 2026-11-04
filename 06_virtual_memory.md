# 06. Virtual Memory

## Main idea
Each process sees a **virtual address space**. The OS and hardware map virtual pages to physical memory, subject to permissions.

## Benefits
- Isolation between processes.
- Flexible allocation and mapping.
- Sharing selected pages when explicitly configured.
- Running programs without keeping every page resident in RAM at once.

## Address translation
The MMU translates virtual addresses using page tables. A **TLB** caches recent translations.

## Page fault
A page fault occurs when an address translation or access cannot be completed under the current mappings/permissions. Some faults can be handled by loading or mapping a page; invalid accesses may terminate a process.

## Key distinction
The same virtual address in two processes can map to different physical pages.

**Review:** What does a TLB miss mean, and why is it not necessarily a page fault?
