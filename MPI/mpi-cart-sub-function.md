---
title: MPI_Cart_sub function
TOCTitle: MPI_Cart_sub function
ms:assetid: 6905d404-820f-440c-b3e3-aad9eed108bb
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473251(v=VS.85)
ms:contentKeyID: 59360797
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CART_SUB
- mpif/MPI_Cart_sub
- mpi/MPI_CART_SUB
dev_langs:
- C++
- C
---

# MPI\_Cart\_sub function

TBD

## Syntax

``` c++
int MPIAPI MPI_Cart_sub(
        MPI_Comm comm,
  _In_  int      *remain_dims,
  _Out_ MPI_Comm *newcomm
);
```

## Parameters

  - *comm*  
    TBD

  - *remain\_dims* \[in\]  
    TBD

  - *newcomm* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_CART_SUB(COMM, REMAIN_DIMS, NEWCOMM, IERROR)
        INTEGER COMM, NEWCOMM, IERROR
        LOGICAL REMAIN_DIMS(*)

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

