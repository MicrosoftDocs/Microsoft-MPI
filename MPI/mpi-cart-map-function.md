---
title: MPI_Cart_map function
TOCTitle: MPI_Cart_map function
ms:assetid: ef78cb00-255d-48fc-a5b5-01cd2395165d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473248(v=VS.85)
ms:contentKeyID: 59360794
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_MAP
- mpif/MPI_Cart_map
- mpi/MPI_CART_MAP
dev_langs:
- C++
- C
---

# MPI\_Cart\_map function

Maps process to Cartesian topology information.

## Syntax

``` c++
int MPIAPI MPI_Cart_map(
        _In_              MPI_Comm comm,
        _In_range_(>=, 0) int      ndims,
        _In_count_(ndims) int      *dims,
        _In_count_(ndims) int      *periods,
        _Out_             int      *newrank
);
```

## Parameters

  - *comm*  
    Input communicator.

  - *ndims*  
    Number of dimensions of Cartesian structure.

  - *dims*  
    Integer array of size *ndims* specifying the number of processes in each coordinate direction.

  - *periods*  
    Logical array of size *ndims* specifying the periodicity specification in each coordinate direction.

  - *newrank* \[out\]  
    reordered rank of the calling process; **MPI\_UNDEFINED** if calling process does not belong to grid

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CART_MAP(COMM, NDIMS, DIMS, PERIODS, NEWRANK, IERROR)
        INTEGER COMM, NDIMS, DIMS(*), NEWRANK, IERROR
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

