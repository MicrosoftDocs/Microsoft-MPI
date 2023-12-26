---
title: MPI_Barrier function
TOCTitle: MPI_Barrier function
ms:assetid: 92ef641a-b65b-4e3b-8f64-98d9c0810b29
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473236(v=VS.85)
ms:contentKeyID: 59360782
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_BARRIER
- mpif/MPI_Barrier
- mpi/MPI_BARRIER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Barrier
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Barrier function, its syntax, parameters, and return value. Understand how it initiates barrier synchronization across group members.
---

# MPI\_Barrier function

Initiates barrier synchronization across all members of a group.

## Syntax

``` c++
int MPIAPI MPI_Barrier(
  _In_ MPI_Comm comm
);
```

## Parameters

  - *comm* \[in\]  
    The communicator to synchronize.
    
    If this is an intracommunicator, the **MPI\_Barrier** function blocks the caller until all group members have called it. The function does not return on any process until all group processes have called the function.
    
    If this is an intercommunicator, the **MPI\_Barrier** function involves two groups. The function returns on processes in one group, group A, only after all members of the other group, group B, have called the function, and vice versa. The function can return for a process before all processes in its own group have called the function.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_BARRIER(COMM, IERROR)
        INTEGER COMM, IERROR
```

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
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

[MPI Collective Functions](mpi-collective-functions.md)

