---
title: MPI_Get_accumulate function
TOCTitle: MPI_Get_accumulate function
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_ACCUMULATE
- mpif/MPI_Get_accumulate
- mpi/MPI_GET_ACCUMULATE
dev_langs:
- C++
- C
description: Master the MPI_Get_accumulate function with this comprehensive guide. Learn about its syntax, parameters, and return values for efficient data operations.
---

# MPI\_Get\_accumulate function

Performs atomic read-modify-write and returns the data before the accumulate operation.

## Syntax

``` c++
int MPIAPI MPI_Get_accumulate(
  _In_  void         *origin_addr,
        int          origin_count,
        MPI_Datatype origin_datatype,
  _Out_ void         *result_addr,
        int          result_count,
        MPI_Datatype result_datatype,
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

  - *result\_addr* \[out\]  
    initial address of result buffer

  - *result\_count*  
    number of entries in result buffer

  - *result\_datatype*  
    datatype of each entry in result buffer

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
    MPI_GET_ACCUMULATE(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, RESULT_ADDR, RESULT_COUNT, RESULT_DATATYPE,
                TARGET_RANK, TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, OP, WIN, IERROR)
        <type> ORIGIN_ADDR(*), RESULT_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE, RESULT_COUNT, RESULT_DATATYPE, TARGET_RANK, TARGET_COUNT,
        TARGET_DATATYPE, OP, WIN, IERROR
```

## Remarks

Accumulate *origin_count* elements of type *origin_datatype* from the origin buffer (*origin_addr*) to the buffer at offset *target_disp*, in the target window specified by *target_rank* and *win*, using the operation *op* and return in the result buffer *result_addr* the content of the target buffer before the accumulation, specified by *target_disp*, *target_count*, and *target_datatype*. The data transferred from origin to target must fit, without truncation, in the target buffer. Likewise, the data copied from target to origin must fit, without truncation, in the result buffer.

The origin and result buffers (*origin_addr* and *result_addr*) must be disjoint. Each datatype argument must be a predefined datatype or a derived datatype where all basic components are of the same predefined datatype. All datatype arguments must be constructed from the same predefined datatype. The operation *op* applies to elements of that predefined type. *target_datatype* must not specify overlapping entries, and the target buffer must fit in the target window or in attached memory in a dynamic window. The operation is executed atomically for each basic datatype.

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

