---
title: MPI_Fetch_and_op function
TOCTitle: MPI_Fetch_and_op function
mtps_version: v=VS.85
f1_keywords:
- MPI_FETCH_AND_OP
- mpif/MPI_Fetch_and_op
- mpi/MPI_FETCH_AND_OP
dev_langs:
- C++
- C
description: Learn about the MPI_Fetch_and_op function on Microsoft's official site. Understand its syntax, parameters, return values, and usage in atomic read-modify-write operations.
---

# MPI\_Fetch\_and\_op function

Performs atomic read-modify-write on one element of data, and returns the data element before the accumulate operation.

## Syntax

``` c++
int MPIAPI MPI_Fetch_and_op(
  _In_  void         *origin_addr,
  _Out_ void         *result_addr,
        MPI_Datatype datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        MPI_Op       op,
        MPI_Win      win
);
```

## Parameters

  - *origin\_addr* \[in\]  
    initial address of buffer

  - *result\_addr* \[out\]  
    initial address of result buffer

  - *datatype*  
    datatype of each entry in origin, result and target buffer

  - *target\_rank*  
    rank of target

  - *target\_disp*  
    displacement from start of window to beginning of target buffer

  - *op*  
    reduce operation

  - *win*  
    window object

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FETCH_AND_OP(ORIGIN_ADDR, RESULT_ADDR, DATATYPE,
                TARGET_RANK, TARGET_DISP, OP, WIN, IERROR)
        <type> ORIGIN_ADDR(*), RESULT_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER DATATYPE, TARGET_RANK, OP, WIN, IERROR
```

## Remarks

Accumulate one element of type *datatype* from the origin buffer (*origin_addr*) to the buffer at offset *target_disp*, in the target window specified by *target_rank* and *win*, using the operation *op* and return in the result buffer *result_addr* the content of the target buffer before the accumulation.

The origin and result buffers (*origin_addr* and *result_addr*) must be disjoint. Any of the predefined operations for [**MPI\_Reduce**](mpi-reduce-function.md), as well as **MPI\_NO\_OP** or **MPI\_REPLACE**, can be specified as op; user-defined functions cannot be used. The datatype argument must be a predefined datatype. The operation is executed atomically.

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

