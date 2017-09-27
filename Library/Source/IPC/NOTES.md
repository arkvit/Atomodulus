# Shared Memory

### No persistant shared memory in Windows
Boost library docs about Native windows shared memory:
> Windows operating system also offers shared memory, but the lifetime of this shared memory is very different to kernel or filesystem lifetime. The shared memory is created backed by the pagefile and it's automatically destroyed when the last process attached to the shared memory is destroyed.

Possible solution to force persistant memory:
> But what you can do is create a service that runs in the background and whose sole purpose is to create the shared memory and keep it open, and then other apps can open and read/write to the memory as needed. If necessary, the service can also create a named mutex/semaphore to provide synchronization when apps access the shared memory. Otherwise, for persistent storage, you have to use a file or the Registry instead.
https://stackoverflow.com/questions/36162521/named-shared-memory-windows-api-c

