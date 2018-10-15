---
title: MPI_Rget function
TOCTitle: MPI_Rget function
mtps_version: v=VS.85
f1_keywords:
- MPI_RGET
- mpif/MPI_Rget
- mpi/MPI_RGET
dev_langs:
- C++
- C
---

# MPI\_Rget function

Request-based RMA get operation.

## Syntax

``` c++
int MPIAPI MPI_Rget(
  _Out_ void         *origin_addr,
        int          origin_count,
        MPI_Datatype origin_datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        int          target_count,
        MPI_Datatype datatype,
        MPI_Win      win,
  _Out_ MPI_Request  *request
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

  - *request* \[out\]  
    RMA request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_RGET(ORIGIN_ADDR, ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK,
                TARGET_DISP, TARGET_COUNT, TARGET_DATATYPE, WIN, REQUEST, IERROR)
        <type> ORIGIN_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER ORIGIN_COUNT, ORIGIN_DATATYPE, TARGET_RANK, TARGET_COUNT, TARGET_DATATYPE, WIN, REQUEST, IERROR
```

## Remarks

[**MPI\_Rget**](mpi-rget-function.md) is similar to [**MPI\_Get**](mpi-get-function.md), except that it allocates a communication request object and associates it with the request handle (the argument *request*) that can be used to wait or test for completion. The completion of an [**MPI\_Rget**](mpi-rget-function.md) operation indicates that the data is available in the origin buffer. If *origin_addr* points to memory attached to a window, then the data becomes available in the private copy of this window.

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

