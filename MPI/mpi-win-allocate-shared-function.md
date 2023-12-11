---
title: MPI_Win_allocate_shared function
TOCTitle: MPI_Win_allocate_shared function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_ALLOCATE_SHARED
- mpif/MPI_Win_allocate_shared
- mpi/MPI_WIN_ALLOCATE_SHARED
dev_langs:
- C++
- C
description: Learn how to create an MPI Window object with the MPI_Win_allocate_shared function. Understand syntax, parameters, and return values for successful implementation.
---

# MPI\_Win\_allocate\_shared function

Creates an MPI Window object that allocates memory, allocated memory can be accessed from all processes in the window’s group with direct load/store instructions.

## Syntax

``` c++
int MPIAPI MPI_Win_allocate_shared(
        MPI_Aint size,
        int      disp_unit,
        MPI_Info info,
        MPI_Comm comm,
  _Out_ void     *baseptr,
  _Out_ MPI_Win  *win
);
```

## Parameters

  - *size*  
    Size of the memory window in bytes.

  - *disp\_unit*  
    Local unit size for displacements, in bytes.

  - *info*  
    Info argument.

  - *comm*  
    Intra-communicator.

  - *baseptr* \[out\]  
    Address of local allocated window segment.

  - *win* \[out\]  
    Window object returned by the call.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_ALLOCATE_SHARED(SIZE, DISP_UNIT, INFO, COMM, BASEPTR, WIN, IERROR)
        <type> BASEPTR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
        INTEGER DISP_UNIT, INFO, COMM, WIN, IERROR
```

## Remarks

This is a collective call executed by all processes in the group of *comm*. On each process, it allocates memory of at least *size* bytes that is shared among all processes in *comm*, and returns a pointer to the locally allocated segment in *baseptr* that can be used for load/store accesses on the calling process. The locally allocated memory can be the target of load/store accesses by remote processes; the base pointers for other processes can be queried using the function [**MPI\_Win\_shared\_query**](mpi-win-shared-query-function.md). The call also returns a window object that can be used by all processes in comm to perform RMA operations. The *size* argument may be different at each process and size = 0 is valid. It is the user’s responsibility to ensure that the communicator *comm* represents a group of processes that can create a shared memory segment that can be accessed by all processes in the group.

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

