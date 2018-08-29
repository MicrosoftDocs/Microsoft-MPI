---
title: MPI_Comm_get_errhandler function
TOCTitle: MPI_Comm_get_errhandler function
ms:assetid: b157e69d-b1ee-4456-940c-decc1d0c95db
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473272(v=VS.85)
ms:contentKeyID: 59360818
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_GET_ERRHANDLER
- mpif/MPI_Comm_get_errhandler
- mpi/MPI_COMM_GET_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Comm\_get\_errhandler function

Get the error handler attached to a communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_get_errhandler(
        MPI_Comm       comm,
  _Out_ MPI_Errhandler *errhandler
);
```

## Parameters

  - *comm*  
    Communicator.

  - *errhandler* \[out\]  
    Handler currently associated with communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_COMM_GET_ERRHANDLER(COMM, ERRHANDLER, IERROR)
        INTEGER COMM, ERRHANDLER, IERROR

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

[MPI Management Functions](mpi-management-functions.md)

