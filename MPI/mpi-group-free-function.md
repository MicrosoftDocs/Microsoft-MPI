---
title: MPI_Group_free function
TOCTitle: MPI_Group_free function
ms:assetid: dd68e143-41fa-4bd9-96d9-9fc36f0b03ab
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473398(v=VS.85)
ms:contentKeyID: 59360934
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_FREE
- mpif/MPI_Group_free
- mpi/MPI_GROUP_FREE
dev_langs:
- C++
- C
description: Learn how to use the MPI_Group_free function in Microsoft's HPC Pack. This guide includes syntax, parameters, return values, and requirements.
---

# MPI\_Group\_free function

Frees a group.

## Syntax

``` c++
int MPIAPI MPI_Group_free(
   _Inout_ MPI_Group *group
);
```

## Parameters

  - *group*  
    Group to free.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran the return value is stored in the IERROR parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_FREE(GROUP, IERROR)
        INTEGER GROUP, IERROR
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

[MPI Group Functions](mpi-group-functions.md)

