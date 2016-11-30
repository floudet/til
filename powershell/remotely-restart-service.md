# Remotely Restart a Service 

The sc.exe program allows to communicate with the Service Controller and installed services, on the local or a remote machine.

For example, to stop the 'NSClientpp' service on the 'myserver' remote machine:

```posh
PS C:\Users\Administrator> sc.exe \\myserver stop 'NSClientpp'

SERVICE_NAME: NSClientpp
        TYPE               : 10  WIN32_OWN_PROCESS
        STATE              : 3  STOP_PENDING
                                (STOPPABLE, NOT_PAUSABLE, IGNORES_SHUTDOWN)
        WIN32_EXIT_CODE    : 0  (0x0)
        SERVICE_EXIT_CODE  : 0  (0x0)
        CHECKPOINT         : 0x2
        WAIT_HINT          : 0x0
```

And to start it:

```posh
PS C:\Users\Administrator> sc.exe \\myserver start 'NSClientpp'

SERVICE_NAME: NSClientpp
        TYPE               : 10  WIN32_OWN_PROCESS
        STATE              : 2  START_PENDING
                                (NOT_STOPPABLE, NOT_PAUSABLE, IGNORES_SHUTDOWN)
        WIN32_EXIT_CODE    : 0  (0x0)
        SERVICE_EXIT_CODE  : 0  (0x0)
        CHECKPOINT         : 0x0
        WAIT_HINT          : 0x7d0
        PID                : 6296
        FLAGS              :
```

