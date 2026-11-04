# 09. File Systems

## What is a file system?
A **file system** organizes persistent data into files and directories and provides interfaces for access and metadata.

## Core concepts
- **File:** named collection of data with metadata.
- **Directory:** maps names to file-system objects.
- **File descriptor:** process-local integer handle for an open file or another I/O resource.
- **Inode (in Unix-like systems):** stores metadata and references to file data, generally not the filename itself.

## Common operations
- `open()` obtains a file descriptor.
- `read()` reads bytes from an open descriptor.
- `write()` writes bytes to an open descriptor.
- `close()` releases the descriptor.

## Caching and persistence
The OS may buffer writes. A successful `write()` does not always mean bytes are already durable on storage; durability can require synchronization operations such as `fsync()`.

**Review:** What is the difference between a filename and a file descriptor?
