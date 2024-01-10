---
title: MPI_Comm_remote_group function
TOCTitle: MPI_Comm_remote_group function
ms:assetid: 25455c7f-a873-4407-838b-9f32b1ecd70a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473278(v=VS.85)
ms:contentKeyID: 59360824
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_REMOTE_GROUP
- mpif/MPI_Comm_remote_group
- mpi/MPI_COMM_REMOTE_GROUP
dev_langs:
- C++
- C
description: Learn about the MPI_Comm_remote_group function, its syntax, parameters, and return values. Ideal for users of HPC Pack and MS-MPI Redistributable Package.
---

# MPI\_Comm\_remote\_group function

Accesses the remote group associated with the given inter-communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_remote_group(
        MPI_Comm  comm,
  _Out_ MPI_Group *group
);
```

## Parameters

  - *comm*  
    Communicator (must be an intercommunicator).

  - *group* \[out\]  
    Remote group of communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_REMOTE_GROUP(COMM, GROUP, IERROR)
        INTEGER COMM, GROUP, IERROR
```

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

