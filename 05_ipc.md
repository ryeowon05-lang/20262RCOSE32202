# 05. Inter-Process Communication (IPC)

## Why IPC?
Processes normally have separate address spaces. **IPC** lets them exchange data and coordinate work.

## Common mechanisms
- **Pipe:** byte stream between endpoints; commonly used between related processes.
- **Message queue:** sends and receives discrete messages.
- **Socket:** communication endpoint, including communication across machines.
- **Shared memory:** multiple processes map a shared region; synchronization is usually needed.

## Message queue example
- `mq_send()` takes a pointer to a buffer containing the message to send.
- `mq_receive()` takes a pointer to a destination buffer in the receiving process, where received bytes are written.

A user-space buffer is not the same thing as a kernel-managed message queue.

**Review:** Why can shared memory be fast, and what race conditions might it introduce?
