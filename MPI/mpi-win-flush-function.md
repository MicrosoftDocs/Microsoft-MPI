---
title: MPI_Win_flush function
TOCTitle: MPI_Win_flush function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FLUSH
- mpif/MPI_Win_flush
- mpi/MPI_WIN_FLUSH
dev_langs:
- C++
- C
description: Master the MPI_Win_flush function with our comprehensive guide. Learn about its syntax, parameters, return values, and its role in RMA operations.
---

# MPI\_Win\_flush function

Completes all outstanding RMA operations initiated by the calling process to the target rank on the specified window. The operations are completed both at the origin and at the target.

## Syntax

``` c++
int MPIAPI MPI_Win_flush(
        int      rank,
        MPI_Win  *win
);
```

## Parameters

  - *rank*  
    Rank of target window.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_FLUSH(RANK, WIN, IERROR)
        INTEGER RANK, WIN, IERROR
```

## Remarks

All flush and sync functions can be called only within passive target epochs.

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

