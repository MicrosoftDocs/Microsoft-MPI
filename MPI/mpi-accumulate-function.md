---
title: MPI_Accumulate function
TOCTitle: MPI_Accumulate function
ms:assetid: 3f580b28-6b45-4294-9351-cf5c6b06807e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502495(v=VS.85)
ms:contentKeyID: 59360767
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ACCUMULATE
- mpif/MPI_Accumulate
- mpi/MPI_ACCUMULATE
dev_langs:
- C++
- C
description: Learn how to use the MPI_Accumulate function for data accumulation in remote memory access with Microsoft's comprehensive guide.
---

# MPI\_Accumulate function

Accumulate data into the target process using remote memory access

## Syntax

``` c++
int MPIAPI MPI_Accumulate(
  _In_ void         *origin_addr,
       int          origin_count,
       MPI_Datatype origin_datatype,
       int          target_rank,
       MPI_Aint     target_disp,
       int          target_count,
       MPI_Datatype datatype,
       MPI_Op       op,
       MPI_Win      win
);
```

## Parameters

  - *origin\_addr* \[in\]  
    initial address of buffer

  - *origin\_count*  
    number of entries in buffer

  - *origin\_datatype*  
    datatype of each buffer entry

  - *target\_rank*  
    rank of target

  - *target\_disp*  
    displacement from start of window to beginning of target buffer

  - *target\_count*  
    number of entries in target buffer

  - *datatype*  
    datatype of each entry in target buffer

  - *op*  
    predefined reduce operation

  - *win*  
    window object

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ACCUMULATE(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, OP, WIN, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE,TARGET_RANK, TARGET_COUNT,
        TARGET_DATATYPE, OP, WIN, IERROR
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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

