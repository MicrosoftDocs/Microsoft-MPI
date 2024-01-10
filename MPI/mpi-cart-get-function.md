---
title: MPI_Cart_get function
TOCTitle: MPI_Cart_get function
ms:assetid: 97aa75cb-7fee-4021-b8cb-63812b0c1ef7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473247(v=VS.85)
ms:contentKeyID: 59360793
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_GET
- mpif/MPI_Cart_get
- mpi/MPI_CART_GET
dev_langs:
- C++
- C
description: Learn about MPI_Cart_get function on Microsoft's site. It retrieves Cartesian topology info associated with a communicator. Perfect for HPC Pack users.
---

# MPI\_Cart\_get function

Retrieves Cartesian topology information associated with a communicator.

## Syntax

``` c++
int MPIAPI MPI_Cart_get(
   MPI_Comm               comm,
   int                    maxdims,
   _Out_cap_(maxdims) int *dims,
   _Out_cap_(maxdims) int *periods,
   _Out_cap_(maxdims) int *coords
);
```

## Parameters

  - *comm*  
    Communicator with cartesian structure.

  - *maxdims*  
    Length of vectors  *dims*, *periods*, and *coords* in the calling program.

  - *dims*  
    Number of processes for each cartesian dimension.

  - *periods*  
    Periodicity (true/false) for each cartesian dimension.

  - *coords*  
    Coordinates of calling process in cartesian structure.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_GET(COMM, MAXDIMS, DIMS, PERIODS, COORDS, IERROR)
        INTEGER COMM, MAXDIMS, DIMS(*), COORDS(*), IERROR
        LOGICAL PERIODS(*)
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

[MPI Process Topology Functions](mpi-process-topology-functions.md)

