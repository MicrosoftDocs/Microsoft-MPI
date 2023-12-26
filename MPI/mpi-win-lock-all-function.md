---
title: MPI_Win_lock_all function
TOCTitle: MPI_Win_lock_all function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_LOCK_ALL
- mpif/MPI_Win_lock_all
- mpi/MPI_WIN_LOCK_ALL
dev_langs:
- C++
- C
description: Explore the MPI_Win_lock_all function in detail. Learn about its syntax, parameters, return values, and usage in RMA operations on Microsoft's official site.
---

# MPI\_Win\_lock\_all function

Starts an RMA access epoch to all processes in a window object, with a lock type of **MPI\_LOCK\_SHARED**.

## Syntax

``` c++
int MPIAPI MPI_Win_lock_all(
   int     assert,
   MPI_Win win
);
```

## Parameters

  - *assert*  
    Used to optimize this call; zero may be used as a default.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_LOCK_ALL(ASSERT, WIN, IERROR)
        INTEGER ASSERT, WIN, IERROR
```

## Remarks

During the epoch, the calling process can access the window memory on all processes in *win* by using RMA operations. A window locked with [**MPI\_Win\_lock\_all**](mpi-win-lock-all-function.md) must be unlocked with [**MPI\_Win\_unlock\_all**](mpi-win-unlock-all-function.md). This routine is not collective — the *all* refers to a lock on all members of the group of the window.

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

