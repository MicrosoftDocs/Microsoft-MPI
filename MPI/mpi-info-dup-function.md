---
title: MPI_Info_dup function
TOCTitle: MPI_Info_dup function
ms:assetid: 99d49571-e529-475c-85fb-fca63cc3e19a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473411(v=VS.85)
ms:contentKeyID: 59360947
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_DUP
- mpif/MPI_Info_dup
- mpi/MPI_INFO_DUP
dev_langs:
- C++
- C
description: Learn about the MPI_Info_dup function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Info\_dup function

Returns a duplicate of the info object.

## Syntax

``` c++
int MPIAPI MPI_Info_dup(
        MPI_Info info,
  _Out_ MPI_Info *newinfo
);
```

## Parameters

  - *info*  
    Info object.

  - *newinfo* \[out\]  
    Duplicate of info object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_DUP(INFO, NEWINFO, IERROR)
        INTEGER INFO, NEWINFO, IERROR
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

[MPI Info Object Functions](mpi-info-object-functions.md)

