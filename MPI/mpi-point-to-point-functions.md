---
title: MPI Point to Point Functions
TOCTitle: MPI Point to Point Functions
ms:assetid: 59F2FC56-63FF-4F3B-895A-9639AD57415D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473446(v=VS.85)
ms:contentKeyID: 59360981
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Point to Point Functions

## In this section

  - [**MPI\_Bsend**](mpi-bsend-function.md)  
    Sends data to a specified process in buffered mode.

  - [**MPI\_Bsend\_init**](mpi-bsend-init-function.md)  
    TBD

  - [**MPI\_Cancel**](mpi-cancel-function.md)  
    TBD

  - [**MPI\_Get\_count**](mpi-get-count-function.md)  
    TBD

  - [**MPI\_Ibsend**](mpi-ibsend-function.md)  
    Initiates a buffered mode send operation and returns a handle to the communication operation.

  - [**MPI\_Iprobe**](mpi-iprobe-function.md)  
    TBD

  - [**MPI\_Improbe**](mpi-improbe-function.md)  
    Probes for a message in a non-blocking way. Provides a mechanism to receive the specific message that was matched regardless of intervening probe/receive operations. The matched message is de-queued off the receive queue, giving the application an opportunity to decide how to receive the message based on the information returned by the non-blocking matching probe operation. The matched message is then received using the [**MPI\_Mrecv**](mpi-mrecv-function.md) or [**MPI\_Imrecv**](mpi-imrecv-function.md) function.

  - [**MPI\_Imrecv**](mpi-imrecv-function.md)  
    Performs a non-blocking receive for a message matched by [**MPI\_Mprobe**](mpi-mprobe-function.md) or [**MPI\_Improbe**](mpi-improbe-function.md).

  - [**MPI\_Irecv**](mpi-irecv-function.md)  
    Initiates a receive operation and returns a handle to the requested communication operation.

  - [**MPI\_Irsend**](mpi-irsend-function.md)  
    Initiates a ready mode send operation and returns a request handle that represents the communication operation.

  - [**MPI\_Isend**](mpi-isend-function.md)  
    Initiates a standard mode send operation and returns a handle to the requested communication operation.

  - [**MPI\_Issend**](mpi-issend-function.md)  
    Initiates a synchronous mode send operation and returns a handle to the requested communication operation.

  - [**MPI\_Mprobe**](mpi-mprobe-function.md)  
    Blocking probes for a message. Provides a mechanism to receive the specific message that was matched regardless of intervening probe/receive operations. The matched message is de-queued off the receive queue, giving the application an opportunity to decide how to receive the message based on the information returned by the matching probe operation. The matched message is then received using the [**MPI\_Mrecv**](mpi-mrecv-function.md) or [**MPI\_Imrecv**](mpi-imrecv-function.md) function.

  - [**MPI\_Mrecv**](mpi-mrecv-function.md)  
    Performs a blocking receive for a message matched by [**MPI\_Mprobe**](mpi-mprobe-function.md) or [**MPI\_Improbe**](mpi-improbe-function.md).

  - [**MPI\_Probe**](mpi-probe-function.md)  
    TBD

  - [**MPI\_Recv**](mpi-recv-function.md)  
    Performs a receive operation and does not return until a matching message is received.

  - [**MPI\_Recv\_init**](mpi-recv-init-function.md)  
    TBD

  - [**MPI\_Request\_free**](mpi-request-free-function.md)  
    TBD

  - [**MPI\_Request\_get\_status**](mpi-request-get-status-function.md)  
    TBD

  - [**MPI\_Rsend**](mpi-rsend-function.md)  
    Performs a ready mode send operation and returns when the send buffer can be safely reused.

  - [**MPI\_Rsend\_init**](mpi-rsend-init-function.md)  
    TBD

  - [**MPI\_Send**](mpi-send-function.md)  
    Performs a standard mode send operation and returns when the send buffer can be safely reused.

  - [**MPI\_Send\_init**](mpi-send-init-function.md)  
    TBD

  - [**MPI\_Sendrecv**](mpi-sendrecv-function.md)  
    TBD

  - [**MPI\_Sendrecv\_replace**](mpi-sendrecv-replace-function.md)  
    TBD

  - [**MPI\_Ssend**](mpi-ssend-function.md)  
    Performs a synchronous mode send operation and returns when the send buffer can be safely reused.

  - [**MPI\_Ssend\_init**](mpi-ssend-init-function.md)  
    TBD

  - [**MPI\_Start**](mpi-start-function.md)  
    TBD

  - [**MPI\_Startall**](mpi-startall-function.md)  
    TBD

  - [**MPI\_Test**](mpi-test-function.md)  
    Tests an outstanding operation for completion.

  - [**MPI\_Test\_cancelled**](mpi-test-cancelled-function.md)  
    TBD

  - [**MPI\_Testall**](mpi-testall-function.md)  
    TBD

  - [**MPI\_Testany**](mpi-testany-function.md)  
    TBD

  - [**MPI\_Testsome**](mpi-testsome-function.md)  
    TBD

  - [**MPI\_Wait**](mpi-wait-function.md)  
    Completes an outstanding operation.

  - [**MPI\_Waitall**](mpi-waitall-function.md)  
    Completes multiple outstanding operations.

  - [**MPI\_Waitany**](mpi-waitany-function.md)  
    Completes one out of several outstanding operations.

  - [**MPI\_Waitsome**](mpi-waitsome-function.md)  
    TBD

  - [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md)  
    Acquires the Microsoft MPI library global lock.

  - [**MSMPI\_Queuelock\_release**](msmpi-queuelock-release-function.md)  
    Releases the Microsoft MPI library global lock.

  - [**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md)  
    Waits until at least one of the operations that is associated with active handles in the list has finished, or the call is interrupted by another thread that calls [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md).

