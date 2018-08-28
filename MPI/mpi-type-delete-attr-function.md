---
title: MPI_Type_delete_attr function
TOCTitle: MPI_Type_delete_attr function
ms:assetid: e0547cdd-85d8-4d28-a6ae-1e48aa811554
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520562(v=VS.85)
ms:contentKeyID: 59361033
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_DELETE_ATTR
- mpif/MPI_Type_delete_attr
- mpi/MPI_TYPE_DELETE_ATTR
dev_langs:
- C++
- C
---

# MPI\_Type\_delete\_attr function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_delete_attr(
   MPI_Datatype datatype,
   int          type_keyval
);
```

## Parameters

  - *datatype*  
    TBD

  - *type\_keyval*  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_DELETE_ATTR(DATATYPE, TYPE_KEYVAL, IERROR)
        INTEGER DATATYPE, TYPE_KEYVAL, IERROR

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

[MPI Caching Functions](mpi-caching-functions.md)

