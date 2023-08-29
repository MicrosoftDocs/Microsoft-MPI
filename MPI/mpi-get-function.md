---
title: MPI_Get function
TOCTitle: MPI_Get function
ms.assetid: 7255cdf7-1fdf-4780-9c50-9c7eb8b28297
ms.mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473378(v=VS.85)
ms.contentKeyID: 59360914
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
  - MPI_GET
  - mpif/MPI_Get
  - mpi/MPI_GET
dev_langs:
  - C++
  - C
description: "Master the MPI_Get Function: Learn to access remote memory windows with Microsoft's Message Passing Interface. Boost your parallel computing skills."
---

# MPI\_Get function

Gets data from a memory window on a remote process.

## Syntax

``` c++
int MPIAPI MPI_Get(
  _Out_ void         *origin_addr,
        int          origin_count,
        MPI_Datatype origin_datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        int          target_count,
        MPI_Datatype datatype,
        MPI_Win      win
);
```

## Parameters

  - *origin\_addr* \[out\]  
    Address of the buffer in which to receive the data.

  - *origin\_count*  
    Number of entries in origin buffer.

  - *origin\_datatype*  
    Datatype of each entry in origin buffer.

  - *target\_rank*  
    Rank of target.

  - *target\_disp*  
    Displacement from window start to the beginning of the target buffer.

  - *target\_count*  
    Number of entries in target buffer.

  - *datatype*  
    Datatype of each entry in target buffer.

  - *win*  
    Window object used for communication.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GET(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, WIN, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

