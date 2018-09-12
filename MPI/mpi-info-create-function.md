﻿---
title: MPI_Info_create function
TOCTitle: MPI_Info_create function
ms:assetid: 95df767e-93a9-4d7c-9d3b-8ed80d5a1b48
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473409(v=VS.85)
ms:contentKeyID: 59360945
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_CREATE
- mpif/MPI_Info_create
- mpi/MPI_INFO_CREATE
dev_langs:
- C++
- C
---

# MPI\_Info\_create function

Creates a new info object.

## Syntax

``` c++
int MPIAPI MPI_Info_create(
  _Out_ MPI_Info *info
);
```

## Parameters

  - *info* \[out\]  
    Info object created.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_CREATE(INFO, IERROR)
        INTEGER INFO, IERROR
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

[MPI Info Object Functions](mpi-info-object-functions.md)

