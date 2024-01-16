---
title: MSMPI_Queuelock_release function
TOCTitle: MSMPI_Queuelock_release function
ms:assetid: C11D4EC4-E2F7-4DF2-A837-6F863A407085
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520624(v=VS.85)
ms:contentKeyID: 59361095
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Queuelock_release
- MSMPI_Queuelock_release
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MSMPI_Queuelock_release
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MSMPI\_Queuelock\_release function

Releases the Microsoft MPI library global lock.

## Syntax

``` c++
void MSMPI_Queuelock_release(
  _In_ MSMPI_Lock_queue *queue
);
```

## Parameters

  - *queue* \[in\]  
    The lock queue structure that represents the calling thread in the queue. This structure was initialized by using the [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md) function.

## Return value

This function does not return a value.

## Remarks

Users of the [**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md) function should release and re-acquire the lock when the function is interrupted, in order to enable the interrupting threads to run.

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

[**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md)

[**MSMPI\_Waitsome\_interruptible**](msmpi-waitsome-interruptible-function.md)

