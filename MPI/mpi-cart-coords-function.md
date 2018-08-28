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
---

# MPI\_Cart\_coords function

TBD

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
    TBD

  - *rank*  
    TBD

  - *maxdims*  
    TBD

  - *coords*  
    TBD

## Return value

TBD

## Fortran

    MPI_CART_COORDS(COMM, RANK, MAXDIMS, COORDS, IERROR)
        INTEGER COMM, RANK, MAXDIMS, COORDS(*), IERROR

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

