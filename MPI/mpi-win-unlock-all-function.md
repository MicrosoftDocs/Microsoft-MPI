---
title: MPI_Win_unlock_all function
TOCTitle: MPI_Win_unlock_all function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_UNLOCK_ALL
- mpif/MPI_Win_unlock_all
- mpi/MPI_WIN_UNLOCK_ALL
dev_langs:
- C++
- C
description: Explore the MPI_Win_unlock_all function on Microsoft's learning platform. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Win\_unlock\_all function

Completes a shared RMA access epoch started by a call to [**MPI\_Win\_lock\_all**](mpi-win-lock-all-function.md) on window. RMA operations issued during this epoch will have completed both at the origin and at the target when the call returns.

## Syntax

``` c++
int MPIAPI MPI_Win_unlock_all(
   MPI_Win win
);
```

## Parameters

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_UNLOCK_ALL(WIN, IERROR)
        INTEGER WIN, IERROR
```

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

