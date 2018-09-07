---
title: MPI_Win_create_errhandler function
TOCTitle: MPI_Win_create_errhandler function
ms:assetid: e15fa101-c1c0-4764-8c8c-05cb829bf8ff
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520597(v=VS.85)
ms:contentKeyID: 59361068
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CREATE_ERRHANDLER
- mpif/MPI_Win_create_errhandler
- mpi/MPI_WIN_CREATE_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Win\_create\_errhandler function

Creates an error handler for use with MPI window objects.

## Syntax

``` c++
int MPIAPI MPI_Win_create_errhandler(
  _In_  MPI_Win_errhandler_fn *function,
  _Out_ MPI_Errhandler        *errhandler
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

    MPI_WIN_CREATE_ERRHANDLER(WIN_ERRHANDLER_FN, ERRHANDLER, IERROR)
        EXTERNAL WIN_ERRHANDLER_FN
        INTEGER ERRHANDLER, IERROR

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

[*MPI\_Win\_errhandler\_fn*](mpi-win-errhandler-fn-callback-function.md)

