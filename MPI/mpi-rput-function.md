---
title: MPI_Rput function
TOCTitle: MPI_Rput function
mtps_version: v=VS.85
f1_keywords:
- MPI_RPUT
- mpif/MPI_Rput
- mpi/MPI_RPUT
dev_langs:
- C++
- C
description: Learn about the MPI_Rput function, its syntax, parameters, and return values. Understand how it differs from MPI_Put and its role in one-sided communications.
---

# MPI\_Rput function

Request-based RMA put operation.

## Syntax

``` c++
int MPIAPI MPI_Rput(
  _In_  void         *origin_addr,
        int          origin_count,
        MPI_Datatype origin_datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        int          target_count,
        MPI_Datatype target_datatype,
        MPI_Win      win,
  _Out_ MPI_Request  *request
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

  - *request* \[out\]  
    RMA request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_RPUT(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, WIN, REQUEST, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK, TARGET_COUNT,
        TARGET_DATATYPE, WIN, REQUEST, IERROR
```

## Remarks

[**MPI\_Rput**](mpi-rput-function.md) is similar to [**MPI\_Put**](mpi-put-function.md), except that it allocates a communication request object and associates it with the request handle (the argument *request*). The completion of an [**MPI\_Rput**](mpi-rput-function.md) operation (i.e., after the corresponding test or wait) indicates that the sender is now free to update the locations in the origin buffer. It does not indicate that the data is available at the target window. If remote completion is required, [**MPI\_Win\_flush**](mpi-win-flush-function.md), [**MPI\_Win\_flush\_all**](mpi-win-flush-all-function.md), [**MPI\_Win\_unlock**](mpi-win-unlock-function.md), or [**MPI\_Win\_unlock\_all**](mpi-win-unlock-all-function.md) can be used.

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

