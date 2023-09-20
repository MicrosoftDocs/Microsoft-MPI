---
title: MPI_Cart_coords function
TOCTitle: MPI_Cart_coords function
ms:assetid: aafb5414-564a-45c6-ad3c-4a83518419c7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473245(v=VS.85)
ms:contentKeyID: 59360791
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_COORDS
- mpif/MPI_Cart_coords
- mpi/MPI_CART_COORDS
dev_langs:
- C++
- C
description: Learn about the MPI_Cart_coords function, its syntax, parameters, and return values. Ideal for understanding process coordinates in cartesian topology.
---

# MPI\_Cart\_coords function

Determines process coords in cartesian topology given rank in group.

## Syntax

``` c++
int MPIAPI MPI_Cart_coords(
   MPI_Comm               comm,
   int                    rank,
   int                    maxdims,
   _Out_cap_(maxdims) int *coords
);
```

## Parameters

  - *comm*  
    Communicator with cartesian structure.

  - *rank*  
    Rank of a process within group of *comm*.

  - *maxdims*  
    Length of vector *coords* in the calling program.

  - *coords*  
    Integer array (of size *maxdims*) containing the Cartesian coordinates of specified process.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_COORDS(COMM, RANK, MAXDIMS, COORDS, IERROR)
        INTEGER COMM, RANK, MAXDIMS, COORDS(*), IERROR
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

