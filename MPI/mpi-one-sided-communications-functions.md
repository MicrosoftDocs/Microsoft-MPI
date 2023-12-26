---
title: MPI One-Sided Communications Functions
TOCTitle: MPI One-Sided Communications Functions
ms:assetid: 5555139A-2EA1-4BD4-954C-5DEBD0B94D43
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473435(v=VS.85)
ms:contentKeyID: 59360971
ms.date: 03/28/2018
mtps_version: v=VS.85
description: Explore MPI One-Sided Communications Functions on Microsoft's learning platform. Understand remote memory access, atomic operations, and RMA epochs.
---

# MPI One-Sided Communications Functions

## In this section

  - [**MPI\_Accumulate**](mpi-accumulate-function.md)  
    Accumulates data into the target process using remote memory access.

  - [**MPI\_Compare\_and\_swap**](mpi-compare-and-swap-function.md)  
    Performs a remote atomic compare and swap operation.

  - [**MPI\_Fetch\_and\_op**](mpi-fetch-and-op-function.md)  
    Performs atomic read-modify-write on one element of data, and returns the data element before the accumulate operation.

  - [**MPI\_Get**](mpi-get-function.md)  
    Gets data from a memory window on a remote process.

  - [**MPI\_Get\_accumulate**](mpi-get-accumulate-function.md)  
    Performs atomic read-modify-write and returns the data before the accumulate operation.

  - [**MPI\_Raccumulate**](mpi-raccumulate-function.md)  
    Request-based RMA accumulate operation.

  - [**MPI\_Rget**](mpi-rget-function.md)  
    Request-based RMA get operation.

  - [**MPI\_Rget\_accumulate**](mpi-rget-accumulate-function.md)  
    Request-based RMA read-modify-write operation returns the data before the accumulate operation.

  - [**MPI\_Rput**](mpi-rput-function.md)  
    Request-based RMA put operation.

  - [**MPI\_Put**](mpi-put-function.md)  
    Puts data into a memory window on a remote process.

  - [**MPI\_Win\_allocate**](mpi-win-allocate-function.md)  
    Creates an MPI Window object that allocates memory.

  - [**MPI\_Win\_allocate\_shared**](mpi-win-allocate-shared-function.md)  
    Creates an MPI Window object that allocates memory, allocated memory can be accessed from all processes in the window’s group with direct load/store instructions.

  - [**MPI\_Win\_attach**](mpi-win-attach-function.md)  
    Attaches a local memory region for remote access within the given window.

  - [**MPI\_Win\_complete**](mpi-win-complete-function.md)  
    Completes an RMA operations begun after an [**MPI\_Win\_start**](mpi-win-start-function.md).

  - [**MPI\_Win\_create**](mpi-win-create-function.md)  
    Creates an MPI Window object for one-sided communication.

  - [**MPI\_Win\_create\_dynamic**](mpi-win-create-dynamic-function.md)  
    Creates a window that allows the user to dynamically control which memory is exposed by the window.

  - [**MPI\_Win\_detach**](mpi-win-detach-function.md)  
    Detaches a previously attached memory region.

  - [**MPI\_Win\_fence**](mpi-win-fence-function.md)  
    Performs an MPI fence synchronization on a MPI window.

  - [**MPI\_Win\_flush**](mpi-win-flush-function.md)  
    Completes all outstanding RMA operations initiated by the calling process to the target rank.

  - [**MPI\_Win\_flush\_all**](mpi-win-flush-all-function.md)  
    Completes operations issued by the calling process to any target on the specified window.

  - [**MPI\_Win\_flush\_local**](mpi-win-flush-local-function.md)  
    Locally completes at the origin all outstanding RMA operations initiated by the calling process to the target process.

  - [**MPI\_Win\_flush\_local\_all**](mpi-win-flush-local-all-function.md)  
    Locally completes at the origin all RMA operations issued by the calling process to any target.

  - [**MPI\_Win\_free**](mpi-win-free-function.md)  
    Frees an MPI RMA window object.

  - [**MPI\_Win\_get\_group**](mpi-win-get-group-function.md)  
    Gets the MPI Group of the window object.

  - [**MPI\_Win\_lock**](mpi-win-lock-function.md)  
    Begins an RMA access epoch at the target process.

  - [**MPI\_Win\_lock\_all**](mpi-win-lock-all-function.md)  
    Starts an RMA access epoch to all processes in window object.

  - [**MPI\_Win\_post**](mpi-win-post-function.md)  
    Starts an RMA exposure epoch.

  - [**MPI\_Win\_shared\_query**](mpi-win-shared-query-function.md)  
    Queries the process-local address for remote memory segments created with [**MPI\_Win\_allocate\_shared**](mpi-win-allocate-shared-function.md).

  - [**MPI\_Win\_start**](mpi-win-start-function.md)  
    Starts an RMA access epoch.

  - [**MPI\_Win\_sync**](mpi-win-sync-function.md)  
    Synchronizes the private and public window copies of win.

  - [**MPI\_Win\_test**](mpi-win-test-function.md)  
    Tests whether an RMA exposure epoch has completed.

  - [**MPI\_Win\_unlock**](mpi-win-unlock-function.md)  
    Completes an RMA access epoch at the target process.

  - [**MPI\_Win\_unlock\_all**](mpi-win-unlock-all-function.md)  
    Completes a shared RMA access epoch started by a call to [**MPI\_Win\_lock\_all**](mpi-win-lock-all-function.md) on a window.

  - [**MPI\_Win\_wait**](mpi-win-wait-function.md)  
    Completes an RMA exposure epoch begun with [**MPI\_Win\_post**](mpi-win-post-function.md).

