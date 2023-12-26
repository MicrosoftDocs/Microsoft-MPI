---
title: MPI_Put function
TOCTitle: MPI_Put function
ms:assetid: 3a25a0d7-eb69-4377-a9ea-4dd89939b798
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473451(v=VS.85)
ms:contentKeyID: 59360986
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PUT
- mpif/MPI_Put
- mpi/MPI_PUT
dev_langs:
- C++
- C
description: Learn how to use the MPI_Put function to put data into a memory window on a remote process at Microsoft's official site.
---

# MPI\_Put function

Put data into a memory window on a remote process.

## Syntax

``` c++
int MPIAPI MPI_Put(
  _In_ void         *origin_addr,
       int          origin_count,
       MPI_Datatype origin_datatype,
       int          target_rank,
       MPI_Aint     target_disp,
       int          target_count,
       MPI_Datatype target_datatype,
       MPI_Win      win
);
```

## Parameters

  - *origin\_addr* \[in\]  
    Initial address of origin buffer.

  - *origin\_count*  
    Number of entries in origin buffer.

  - *origin\_datatype*  
    Datatype of each entry in origin buffer.

  - *target\_rank*  
    Rank of target.

  - *target\_disp*  
    Displacement from start of window to target buffer.

  - *target\_count*  
    Number of entries in target buffer.

  - *target\_datatype*  
    Datatype of each entry in target buffer.

  - *win*  
    Window object used for communication.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_PUT(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, WIN, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK, TARGET_COUNT,
        TARGET_DATATYPE, WIN, IERROR
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

