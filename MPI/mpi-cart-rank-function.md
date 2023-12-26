---
title: MPI_Cart_rank function
TOCTitle: MPI_Cart_rank function
ms:assetid: 84c507f8-bca9-4a92-befb-9f48555f2544
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473249(v=VS.85)
ms:contentKeyID: 59360795
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_RANK
- mpif/MPI_Cart_rank
- mpi/MPI_CART_RANK
dev_langs:
- C++
- C
description: Learn about the MPI_Cart_rank function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements for successful implementation.
---

# MPI\_Cart\_rank function

Determines process rank in communicator given Cartesian location.

## Syntax

``` c++
int MPIAPI MPI_Cart_rank(
        MPI_Comm comm,
  _In_  int      *coords,
  _Out_ int      *rank
);
```

## Parameters

  - *comm*  
    Communicator with cartesian structure.

  - *coords* \[in\]  
    Integer array (of size *ndims*, the number of dimensions of the Cartesian topology associated with *comm*) specifying the cartesian coordinates of a process.

  - *rank* \[out\]  
    Rank of specified process.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_RANK(COMM, COORDS, RANK, IERROR)
        INTEGER COMM, COORDS(*), RANK, IERROR
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

[MPI Process Topology Functions](mpi-process-topology-functions.md)

