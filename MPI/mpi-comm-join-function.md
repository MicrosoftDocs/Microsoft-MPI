---
title: MPI_Comm_join function
TOCTitle: MPI_Comm_join function
ms:assetid: 3c07220f-07c9-4fa4-ba9f-52160c29100e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473276(v=VS.85)
ms:contentKeyID: 59360822
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_JOIN
- mpif/MPI_Comm_join
- mpi/MPI_COMM_JOIN
dev_langs:
- C++
- C
description: Learn how to create a communicator with MPI_Comm_join function on Microsoft's platform. Understand syntax, parameters, return values, and requirements.
---

# MPI\_Comm\_join function

Creates a communicator by joining two processes connected by a socket.

## Syntax

``` c++
int MPIAPI MPI_Comm_join(
        int      fd,
  _Out_ MPI_Comm *intercomm
);
```

## Parameters

  - *fd*  
    Socket file descriptor.

  - *intercomm* \[out\]  
    New intercommunicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_JOIN(FD, INTERCOMM, IERROR)
        INTEGER FD, INTERCOMM, IERROR
```

## Remarks

The socket must be quiescent before [**MPI\_Comm\_join**](mpi-comm-join-function.md) is called and after [**MPI\_Comm\_join**](mpi-comm-join-function.md) returns. More specifically, on entry to [**MPI\_Comm\_join**](mpi-comm-join-function.md), a read on the socket will not read any data that was written to the socket before the remote process called [**MPI\_Comm\_join**](mpi-comm-join-function.md).

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

[MPI Process Management Functions](mpi-process-management-functions.md)

