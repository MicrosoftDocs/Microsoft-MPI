﻿---
title: MPI_Add_error_code function
TOCTitle: MPI_Add_error_code function
ms:assetid: 3d04e050-5fdc-482f-8913-437eb6b7d8bc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502498(v=VS.85)
ms:contentKeyID: 59360770
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ADD_ERROR_CODE
- mpif/MPI_Add_error_code
- mpi/MPI_ADD_ERROR_CODE
dev_langs:
- C++
- C
---

# MPI\_Add\_error\_code function

Add and MPI error code to an MPI error class

## Syntax

``` c++
int MPIAPI MPI_Add_error_code(
        int errorclass,
  _Out_ int *errorcode
);
```

## Parameters

  - *errorclass*  
    Error class to add an error code.

  - *errorcode* \[out\]  
    New error code for this error class.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ADD_ERROR_CODE(ERRORCLASS, ERRORCODE, IERROR)
        INTEGER ERRORCLASS, ERRORCODE, IERROR
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

