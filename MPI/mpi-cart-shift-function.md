---
title: MPI_Cart_shift function
TOCTitle: MPI_Cart_shift function
ms:assetid: 35d82504-3fdd-4fe4-afa6-27e41b390786
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473250(v=VS.85)
ms:contentKeyID: 59360796
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_SHIFT
- mpif/MPI_Cart_shift
- mpi/MPI_CART_SHIFT
dev_langs:
- C++
- C
description: Learn about MPI_Cart_shift function on Microsoft's official site. Understand its syntax, parameters, return values, and its role in MPI Process Topology Functions.
---

# MPI\_Cart\_shift function

Returns the shifted source and destination ranks, given a shift direction and amount.

## Syntax

``` c++
int MPIAPI MPI_Cart_shift(
        MPI_Comm comm,
        int      direction,
        int      disp,
  _Out_ int      *rank_source,
  _Out_ int      *rank_dest
);
```

## Parameters

  - *comm*  
    Communicator with cartesian structure.

  - *direction*  
    Coordinate dimension of shift.

  - *disp*  
    Displacement (> 0: upwards shift, < 0: downwards shift).

  - *rank\_source* \[out\]  
    Rank of source process.

  - *rank\_dest* \[out\]  
    Rank of destination process.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_SHIFT(COMM, DIRECTION, DISP, RANK_SOURCE, RANK_DEST, IERROR)
        INTEGER COMM, DIRECTION, DISP, RANK_SOURCE, RANK_DEST, IERROR
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

