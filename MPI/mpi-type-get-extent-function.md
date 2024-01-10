---
title: MPI_Type_get_extent function
TOCTitle: MPI_Type_get_extent function
ms:assetid: c0c7644d-9301-4e93-80ee-074280af22bb
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520571(v=VS.85)
ms:contentKeyID: 59361042
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_EXTENT
- mpif/MPI_Type_get_extent
- mpi/MPI_TYPE_GET_EXTENT
dev_langs:
- C++
- C
description: Learn about MPI_Type_get_extent function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Type\_get\_extent function

Gets the lower bound and extent for a datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_get_extent(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *lb,
  _Out_ MPI_Aint     *extent
);
```

## Parameters

  - *datatype*  
    Datatype to get information on.

  - *lb* \[out\]  
    Lower bound of datatype.

  - *extent* \[out\]  
    Extent of datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_GET_EXTENT(DATATYPE, LB, EXTENT, IERROR)
        INTEGER DATATYPE, IERROR
        INTEGER(KIND = MPI_ADDRESS_KIND) LB, EXTENT
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

[MPI Datatype Functions](mpi-datatype-functions.md)

