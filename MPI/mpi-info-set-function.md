---
title: MPI_Info_set function
TOCTitle: MPI_Info_set function
ms:assetid: 276f8c2d-61e3-46c4-9977-cb5781d065c1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473418(v=VS.85)
ms:contentKeyID: 59360954
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_SET
- mpif/MPI_Info_set
- mpi/MPI_INFO_SET
dev_langs:
- C++
- C
description: Learn how to add a (key,value) pair to the info object using MPI_Info_set function on Microsoft's official site.
---

# MPI\_Info\_set function

Adds a (key,value) pair to the info object.

## Syntax

``` c++
int MPIAPI MPI_Info_set(
       MPI_Info info,
  _In_ char     *key,
  _In_ char     *value
);
```

## Parameters

  - *info*  
    Info object.

  - *key* \[in\]  
    Key.

  - *value* \[in\]  
    Value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_SET(INFO, KEY, VALUE, IERROR)
        INTEGER INFO, IERROR
        CHARACTER*(*) KEY, VALUE
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

