---
title: MSMPI_Lock_queue structure
TOCTitle: MSMPI_Lock_queue structure
ms:assetid: F33F11EA-F1D9-4E3C-AB02-A810F19CA02D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520622(v=VS.85)
ms:contentKeyID: 59361093
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Lock_queue
- mpi/PMSMPI_Lock_queue
- MSMPI_Lock_queue
- PMSMPI_Lock_queue
dev_langs:
- C++
- C
api_location:
- mpi.h
api_name:
- MSMPI_Lock_queue
api_type:
- HeaderDef
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MSMPI\_Lock\_queue structure

An opaque structure representing a thread in the Microsoft MPI lock queue.

## Syntax

``` c++
typedef struct _MSMPI_Lock_queue {
  volatile struct _MSMPI_LOCK_QUEUE  *next;
  volatile  MPI_Aint                flags;
} MSMPI_Lock_queue, *PMSMPI_Lock_queue;
```

## Members

  - **next**  
    Points to the next entry in the lock queue.

  - **flags**  
    A flag used by the lock queue implementation for synchronization.

## Remarks

Each thread calling the [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md) creates a unique instance of a **MSMPI\_Lock\_queue** structure. We recommend that you allocate the **MSMPI\_Lock\_queue** structure on the thread’s stack.

> [!IMPORTANT]
> This structure must be treated as opaque by callers.

 

## Requirements

<table>
<colgroup>
<col  />
<col  />
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
</tbody>
</table>


## See also

[MPI Structs](mpi-structs.md)

[**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md)

[**MSMPI\_Queuelock\_release**](msmpi-queuelock-release-function.md)

