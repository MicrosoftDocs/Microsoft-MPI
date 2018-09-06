---
title: MPI_Type_free_keyval function
TOCTitle: MPI_Type_free_keyval function
ms:assetid: 0d27efc5-9246-410f-b922-856888c77121
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520567(v=VS.85)
ms:contentKeyID: 59361038
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_FREE_KEYVAL
- mpif/MPI_Type_free_keyval
- mpi/MPI_TYPE_FREE_KEYVAL
dev_langs:
- C++
- C
---

# MPI\_Type\_free\_keyval function

Frees an attribute key for datatypes.

## Syntax

``` c++
int MPIAPI MPI_Type_free_keyval(
  _Inout_ int *type_keyval
);
```

## Parameters

  - *type\_keyval* \[in, out\]  
    Key value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_FREE_KEYVAL(TYPE_KEYVAL, IERROR)
        INTEGER TYPE_KEYVAL, IERROR

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

