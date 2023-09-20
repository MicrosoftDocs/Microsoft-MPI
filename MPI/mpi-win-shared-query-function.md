---
title: MPI_Win_shared_query function
TOCTitle: MPI_Win_shared_query function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_SHARED_QUERY
- mpif/MPI_Win_shared_query
- mpi/MPI_WIN_SHARED_QUERY
dev_langs:
- C++
- C
description: Learn about the MPI_Win_shared_query function, its syntax, parameters, and return values. Ideal for understanding remote memory segments in MPI.
---

# MPI\_Win\_shared\_query function

Queries the process-local address for remote memory segments created with [**MPI\_Win\_allocate\_shared**](mpi-win-allocate-shared-function.md).

## Syntax

``` c++
int MPIAPI MPI_Win_shared_query(
        MPI_Win  *win
        int      rank,
  _Out_ MPI_Aint *size,
  _Out_ int      *disp_unit,
  _Out_ void     *baseptr
);
```

## Parameters

  - *win* \[in\]  
    Shared memory window object.

  - *rank*  
    Rank in the group of window win (non-negative integer) or **MPI\_PROC\_NULL**.

  - *size* \[out\]   
    Size of the window segment.

  - *disp\_unit*  \[out\]   
    Local unit size for displacements, in bytes.

  - *baseptr* \[out\]  
    Address for load/store access to window segment.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_SHARED_QUERY(WIN, RANK, SIZE, DISP_UNIT, BASEPTR, IERROR)
        INTEGER WIN, RANK, DISP_UNIT, IERROR
        INTEGER (KIND=MPI_ADDRESS_KIND) SIZE, BASEPTR
```

## Remarks

This function queries the process-local address for remote memory segments created with [**MPI\_Win\_allocate\_shared**](mpi-win-allocate-shared-function.md). This function can return different process-local addresses for the same physical memory on different processes.

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

