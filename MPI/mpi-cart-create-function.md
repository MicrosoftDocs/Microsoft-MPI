---
title: MPI_Cart_create function
TOCTitle: MPI_Cart_create function
ms:assetid: 6d87963c-d013-4944-bd45-78c016477969
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473246(v=VS.85)
ms:contentKeyID: 59360792
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_CREATE
- mpif/MPI_Cart_create
- mpi/MPI_CART_CREATE
dev_langs:
- C++
- C
---

# MPI\_Cart\_create function

Makes a new communicator to which topology information has been attached.

## Syntax

``` c++
int MPIAPI MPI_Cart_create(
        MPI_Comm              comm_old,
        int                   ndims,
        _In_count_(ndims) int *dims,
        _In_count_(ndims) int *periods,
        int                   reorder,
  _Out_ MPI_Comm              *comm_cart
);
```

## Parameters

  - *comm\_old*  
    Input communicator.

  - *ndims*  
    Number of dimensions of cartesian grid.

  - *dims*  
    Integer array of size *ndims* specifying the number of processes in each dimension.

  - *periods*  
    Logical array of size ndims specifying whether the grid is periodic (true) or not (false) in each dimension.

  - *reorder*  
    Ranking may be reordered (true) or not (false).

  - *comm\_cart* \[out\]  
    Communicator with new cartesian topology.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_CREATE(COMM_OLD, NDIMS, DIMS, PERIODS, REORDER, COMM_CART, IERROR)
        INTEGER COMM_OLD, NDIMS, DIMS(*), COMM_CART, IERROR
        LOGICAL PERIODS(*), REORDER
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

