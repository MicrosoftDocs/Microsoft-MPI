---
title: MPI_Get_version function
TOCTitle: MPI_Get_version function
ms:assetid: addf93e6-793d-45b0-b48b-e2da0d3791a1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473383(v=VS.85)
ms:contentKeyID: 59360919
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_VERSION
- mpif/MPI_Get_version
- mpi/MPI_GET_VERSION
dev_langs:
- C++
- C
description: Learn about the MPI_Get_version function on Microsoft's official site. Discover its syntax, parameters, return value, and related MPI management functions.
---

# MPI\_Get\_version function

Returns the version number of MPI.

## Syntax

``` c++
int MPIAPI MPI_Get_version(
  _Out_ int *version,
  _Out_ int *subversion
);
```

## Parameters

  - *version* \[out\]  
    Version of MPI.

  - *subversion* \[out\]  
    Subversion of MPI.

## Return value

**MPI\_SUCCESS**

## Fortran

``` FORTRAN
    MPI_GET_VERSION(VERSION, SUBVERSION, IERROR)
        INTEGER VERSION, SUBVERSION, IERROR
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

