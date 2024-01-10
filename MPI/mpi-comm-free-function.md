---
title: MPI_Comm_free function
TOCTitle: MPI_Comm_free function
ms:assetid: fd2c2e53-09dc-4438-bec8-9c4384db4497
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473269(v=VS.85)
ms:contentKeyID: 59360815
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_FREE
- mpif/MPI_Comm_free
- mpi/MPI_COMM_FREE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_free
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to free a communicator with the MPI_Comm_free function. Understand its syntax, parameters, return values, and application in both intra and intercommunicators.
---

# MPI\_Comm\_free function

Frees a communicator that is allocated with the [**MPI\_Comm\_dup**](mpi-comm-dup-function.md), [**MPI\_Comm\_create**](mpi-comm-create-function.md), or [**MPI\_Comm\_split**](mpi-comm-split-function.md) functions.

## Syntax

``` c++
int MPIAPI MPI_Comm_free(
   _Inout_ MPI_Comm *comm
);
```

## Parameters

  - *comm*  
    The pointer to a communicator handle to free.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_FREE(COMM,IERROR)
        INTEGER COMM, IERROR
```

## Remarks

This collective operation marks the communication object for deallocation. The handle is set to **MPI\_COMM\_NULL**. Any pending operations that use this communicator finish normally. The object is not deallocated until there are no active references to it.

This function applies to both intracommunicators and intercommunicators.

The delete callback functions for all cached attributes are called in an indeterminate order.

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

[MPI Communicator Functions](mpi-communicator-functions.md)

[**MPI\_Comm\_create**](mpi-comm-create-function.md)

[**MPI\_Comm\_split**](mpi-comm-split-function.md)

[**MPI\_Comm\_dup**](mpi-comm-dup-function.md)

