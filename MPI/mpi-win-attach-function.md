---
title: MPI_Win_attach function
TOCTitle: MPI_Win_attach function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_ATTACH
- mpif/MPI_Win_attach
- mpi/MPI_WIN_ATTACH
dev_langs:
- C++
- C
description: Learn about the MPI_Win_attach function for remote memory access within a given window. Understand its syntax, parameters, and return values.
---

# MPI\_Win\_attach function

Attaches a local memory region for remote access within the given window.

## Syntax

``` c++
int MPIAPI MPI_Win_attach(
   MPI_Win  win,
   void*    base,
   MPI_Aint size
);
```

## Parameters

  - *win* \[in\]  
    Window object.

  - *base* \[in\]  
    Initial address of memory to be attached.

  - *size* \[in\]   
    Size of memory to be attached in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_ATTACH(WIN, BASE, SIZE, IERROR)
        INTEGER WIN, IERROR
        <type> BASE(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
```

## Remarks

Attaches a local memory region beginning at *base* for remote access within the given window. The memory region specified must not contain any part that is already attached to the window *win*, that is, attaching overlapping memory concurrently within the same window is erroneous. The argument win must be a window that was created with [**MPI\_Win\_create\_dynamic**](mpi-win-create-dynamic-function.md). The local memory region attached to the window consists of size bytes, starting at address base. In C, base is the starting address of a memory region. In Fortran, one can pass the first element of a memory region or a whole array, which must be *simply contiguous*. Multiple (but non-overlapping) memory regions may be attached to the same window.

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

