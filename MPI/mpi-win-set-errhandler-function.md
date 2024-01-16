---
title: MPI_Win_set_errhandler function
TOCTitle: MPI_Win_set_errhandler function
ms:assetid: 96d06273-5afa-4b3a-8a87-62be3775c822
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520612(v=VS.85)
ms:contentKeyID: 59361083
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_SET_ERRHANDLER
- mpif/MPI_Win_set_errhandler
- mpi/MPI_WIN_SET_ERRHANDLER
dev_langs:
- C++
- C
description: Learn how to set error handlers for MPI windows objects using MPI_Win_set_errhandler function. Includes syntax, parameters, and return values.
---

# MPI\_Win\_set\_errhandler function

Sets error handler for MPI windows object.

## Syntax

``` c++
int MPIAPI MPI_Win_set_errhandler(
   MPI_Win        win,
   MPI_Errhandler errhandler
);
```

## Parameters

  - *win*  
    Window object.

  - *errhandler*  
    New error handler for the window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_SET_ERRHANDLER(WIN, ERRHANDLER, IERROR)
        INTEGER WIN, ERRHANDLER, IERROR
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

[MPI Management Functions](mpi-management-functions.md)

