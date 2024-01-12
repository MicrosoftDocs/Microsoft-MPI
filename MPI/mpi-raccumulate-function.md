---
title: MPI_Raccumulate function
TOCTitle: MPI_Raccumulate function
mtps_version: v=VS.85
f1_keywords:
- MPI_RACCUMULATE
- mpif/MPI_Raccumulate
- mpi/MPI_RACCUMULATE
dev_langs:
- C++
- C
description: Learn about the MPI_Raccumulate function on Microsoft's official site. Understand its syntax, parameters, return values, and its role in one-sided communications functions.
---

# MPI\_Raccumulate function

Request-based RMA accumulate operation.

## Syntax

``` c++
int MPIAPI MPI_Raccumulate(
  _In_  void         *origin_addr,
        int          origin_count,
        MPI_Datatype origin_datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        int          target_count,
        MPI_Datatype datatype,
        MPI_Op       op,
        MPI_Win      win,
  _Out_ MPI_Request  *request
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

  - *request* \[out\]  
    RMA request

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_RACCUMULATE(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, OP, WIN, REQUEST, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE,TARGET_RANK, TARGET_COUNT,
        TARGET_DATATYPE, OP, WIN, REQUEST, IERROR
```

## Remarks

[**MPI\_Raccumulate**](mpi-raccumulate-function.md) is similar to [**MPI\_Accumulate**](mpi-accumulate-function.md), except that it allocates a communication request object and associates it with the request handle (the argument *request*) that can be used to wait or test for completion. The completion of an [**MPI\_Raccumulate**](mpi-raccumulate-function.md) operation indicates that the origin buffer is free to be updated. It does not indicate that the operation has completed at the target window.

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

