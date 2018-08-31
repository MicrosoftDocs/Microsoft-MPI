---
title: MPI_Errhandler_free function
TOCTitle: MPI_Errhandler_free function
ms:assetid: ae6c446a-968a-40a4-b213-1b70511dc85b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473295(v=VS.85)
ms:contentKeyID: 59360841
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ERRHANDLER_FREE
- mpif/MPI_ERRHANDLER_FREE
- mpi/MPI_ERRHANDLER_FREE
dev_langs:
- C++
- C
---

# MPI\_Errhandler\_free function

Frees an MPI-style errorhandler.

## Syntax

``` c++
int MPIAPI MPI_Errhandler_free(
   _Inout_ MPI_Errhandler *errhandler
);
```

## Parameters

  - *errhandler*  
    MPI error handler.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_ERRHANDLER_FREE(ERRHANDLER, IERROR)
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
<td>Mpi.h</td>
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

