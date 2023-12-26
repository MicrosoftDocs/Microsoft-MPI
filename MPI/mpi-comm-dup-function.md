---
title: MPI_Comm_dup function
TOCTitle: MPI_Comm_dup function
ms:assetid: f23804db-a2b4-478d-8b1d-c628b52e864d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473267(v=VS.85)
ms:contentKeyID: 59360813
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_DUP
- mpif/MPI_Comm_dup
- mpi/MPI_COMM_DUP
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_dup
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to duplicate an existing communicator with MPI_Comm_dup function. Understand its syntax, parameters, return values, and application in parallel processes.
---

# MPI\_Comm\_dup function

Duplicates an existing communicator with associated key values. For each key value, the respective copy callback function determines the attribute value that is associated with this key in the new communicator. The copy callback can, for example, delete the attribute from the new communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_dup(
        MPI_Comm comm,
  _Out_ MPI_Comm *newcomm
);
```

## Parameters

  - *comm*  
    The communicator to duplicate.

  - *newcomm* \[out\]  
    On return, contains a handle to a new communicator. The new communicator has the same group or groups and any copied cached information from the source, but it contains new context information.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_DUP(COMM,NEWCOMM,IERROR)
        INTEGER COMM, NEWCOMM, IERROR
```

## Remarks

This function creates a duplicate communication space that has the same properties as the original communicator. This includes any attributes and topologies. This function is valid even if there are pending point-to-point communications that involve the source communicator.

A user can call the **MPI\_Comm\_dup** function at the beginning of the parallel process and later free the duplicate communicator by using the [**MPI\_Comm\_free**](mpi-comm-free-function.md) function. Other models of communicator management are also possible.

This function applies to both intracommunicators and intercommunicators.

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

[MPI Communicator Functions](mpi-communicator-functions.md)

