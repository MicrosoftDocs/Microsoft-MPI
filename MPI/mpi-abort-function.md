---
title: MPI_Abort function
TOCTitle: MPI_Abort function
ms:assetid: 5d2710ad-44c9-4d3a-be7e-70d8dd27b997
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502494(v=VS.85)
ms:contentKeyID: 59360766
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ABORT
- mpif/MPI_Abort
- mpi/MPI_ABORT
dev_langs:
- C++
- C
description: Learn about the MPI_Abort function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements for successful execution.
---

# MPI\_Abort function

Terminates MPI execution environment

## Syntax

``` c++
int MPIAPI MPI_Abort(
   MPI_Comm comm,
   int      errorcode
);
```

## Parameters

  - *comm*  
    communicator of tasks to abort

  - *errorcode*  
    error code to return to invoking environment

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ABORT(COMM, ERRORCODE, IERROR)
        INTEGER COMM, ERRORCODE, IERROR
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

[MPI Management Functions](mpi-management-functions.md)

