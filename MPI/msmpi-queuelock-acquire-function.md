---
title: MSMPI_Queuelock_acquire function
TOCTitle: MSMPI_Queuelock_acquire function
ms:assetid: 185CFDF0-FA10-41A8-A8B1-E4C180E8A175
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520623(v=VS.85)
ms:contentKeyID: 59361094
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Queuelock_acquire
- MSMPI_Queuelock_acquire
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MSMPI_Queuelock_acquire
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MSMPI_Queuelock_acquire function in Microsoft MPI library for FIFO serialization of callers. Includes syntax, parameters, and usage tips.
---

# MSMPI\_Queuelock\_acquire function

Acquires the Microsoft MPI library global lock. The lock queue is a First-In-First-Out (FIFO) queue.

## Syntax

``` c++
void MSMPI_Queuelock_acquire(
  _Out_ MSMPI_Lock_queue *queue
);
```

## Parameters

  - *queue* \[out\]  
    Points to a user-supplied [**MSMPI\_Lock\_queue**](msmpi-lock-queue-structure.md) structure that represents the position of the calling thread in the queue until the user releases the lock by using the [**MSMPI\_Queuelock\_release**](msmpi-queuelock-release-function.md) function.

## Return value

This function does not return a value.

## Remarks

The behavior of this function depends on the level of thread support in use. When the thread support is **MPI\_THREAD\_SERIALIZED** or lower, this function acquires the Microsoft MPI global lock, which provides FIFO serialization of callers and interrupts any [**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md) function calls that are in-progress.

Applications should normally allocate the queue structure on the stack each time they acquire the lock.

To avoid errors when threads use [**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md) in multi-threaded applications, all threads must acquire the global lock before they call MPI functions.

This function is an extension to the standard.

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Mpi.h</td>
</tr>
<tr class="odd">
<td><p>Library</p></td>
<td>Msmpi.lib</td>
</tr>
<tr class="even">
<td><p>DLL</p></td>
<td>Msmpi.dll</td>
</tr>
</tbody>
</table>


## See also

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

[**MSMPI\_Lock\_queue**](msmpi-lock-queue-structure.md)

[**MSMPI\_Queuelock\_release**](msmpi-queuelock-release-function.md)

[**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md)

