---
title: MPI_Comm_create_errhandler function
TOCTitle: MPI_Comm_create_errhandler function
ms:assetid: 43a8f33f-1b5c-451f-8d6d-1852b73703d1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473262(v=VS.85)
ms:contentKeyID: 59360808
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_CREATE_ERRHANDLER
- mpif/MPI_Comm_create_errhandler
- mpi/MPI_COMM_CREATE_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Comm\_create\_errhandler function

Create a communicator error handler.

## Syntax

``` c++
int MPIAPI MPI_Comm_create_errhandler(
  _In_  MPI_Comm_errhandler_function *function,
  _Out_ MPI_Errhandler               *errhandler
);
```

## Parameters

  - *function* \[in\]  
    User defined error handling procedure.

  - *errhandler* \[out\]  
    MPI error handler.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_CREATE_ERRHANDLER(COMM_ERRHANDLER_FN, ERRHANDLER, IERROR)
        EXTERNAL COMM_ERRHANDLER_FN
        INTEGER ERRHANDLER, IERROR
```

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

[MPI Management Functions](mpi-management-functions.md)

