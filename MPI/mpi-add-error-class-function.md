---
title: MPI_Add_error_class function
TOCTitle: MPI_Add_error_class function
ms:assetid: dcef3d57-8b0f-4cc9-b2d0-04f8f9491304
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502497(v=VS.85)
ms:contentKeyID: 59360769
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ADD_ERROR_CLASS
- mpif/MPI_Add_error_class
- mpi/MPI_ADD_ERROR_CLASS
dev_langs:
- C++
- C
---

# MPI\_Add\_error\_class function

Add an MPI error class to the known classes

## Syntax

``` c++
int MPIAPI MPI_Add_error_class(
  _Out_ int *errorclass
);
```

## Parameters

  - *errorclass* \[out\]  
    New error class

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ADD_ERROR_CLASS(ERRORCLASS, IERROR)
        INTEGER ERRORCLASS, IERROR
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

