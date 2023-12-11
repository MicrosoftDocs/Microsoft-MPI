---
title: MPI_Win_allocate function
TOCTitle: MPI_Win_allocate function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_ALLOCATE
- mpif/MPI_Win_allocate
- mpi/MPI_WIN_ALLOCATE
dev_langs:
- C++
- C
description: Learn how to create an MPI Window object with the MPI_Win_allocate function on Microsoft's official site. Understand syntax, parameters, and return values.
---

# MPI\_Win\_allocate function

Creates an MPI Window object that allocates memory.

## Syntax

``` c++
int MPIAPI MPI_Win_allocate(
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
    Communicator.

  - *baseptr* \[out\]  
    Initial address of the memory window.

  - *win* \[out\]  
    Window object returned by the call.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_ALLOCATE(SIZE, DISP_UNIT, INFO, COMM, BASEPTR, WIN, IERROR)
        <type> BASEPTR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
        INTEGER DISP_UNIT, INFO, COMM, WIN, IERROR
```

## Remarks

This is a collective call executed by all processes in the group of *comm*. On each process, it allocates memory of at least *size* bytes, returns a pointer to it, and returns a window object that can be used by all processes in comm to perform RMA operations. The returned memory consists of *size* bytes local to each process, starting at address baseptr and is associated with the window as if the user called [**MPI\_Win\_create**](mpi-win-create-function.md) on existing memory. The *size* argument may be different at each process and *size = 0* is valid; however, a library might allocate and expose more memory in order to create a fast, globally symmetric allocation.

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

