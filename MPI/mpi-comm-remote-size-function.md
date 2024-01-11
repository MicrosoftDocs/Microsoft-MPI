---
title: MPI_Comm_remote_size function
TOCTitle: MPI_Comm_remote_size function
ms:assetid: 9705a575-9a21-4684-991a-9f3337636b53
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473279(v=VS.85)
ms:contentKeyID: 59360825
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_REMOTE_SIZE
- mpif/MPI_Comm_remote_size
- mpi/MPI_COMM_REMOTE_SIZE
dev_langs:
- C++
- C
description: Learn about the MPI_Comm_remote_size function, its syntax, parameters, and return value. Ideal for users of HPC Pack and MS-MPI Redistributable Package.
---

# MPI\_Comm\_remote\_size function

Determines the size of the remote group associated with an inter-communictor.

## Syntax

``` c++
int MPIAPI MPI_Comm_remote_size(
        MPI_Comm comm,
  _Out_ int      *size
);
```

## Parameters

  - *comm*  
    Communicator.

  - *size* \[out\]  
    Number of processes in the remote group of *comm*.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_REMOTE_SIZE(COMM, SIZE, IERROR)
        INTEGER COMM, SIZE, IERROR
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

