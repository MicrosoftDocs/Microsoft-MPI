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

TBD

## Syntax

``` c++
int MPIAPI MPI_Cart_map(
        MPI_Comm              comm,
        int                   ndims,
        _In_count_(ndims) int *dims,
        _In_count_(ndims) int *periods,
  _Out_ int                   *newrank
);
```

## Parameters

  - *comm*  
    TBD

  - *ndims*  
    TBD

  - *dims*  
    TBD

  - *periods*  
    TBD

  - *newrank* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_CART_MAP(COMM, NDIMS, DIMS, PERIODS, NEWRANK, IERROR)
        INTEGER COMM, NDIMS, DIMS(*), NEWRANK, IERROR
        LOGICAL PERIODS(*)

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

