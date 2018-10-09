---
title: MPI_Win_flush_local function
TOCTitle: MPI_Win_flush_local function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FLUSH_LOCAL
- mpif/MPI_Win_flush_local
- mpi/MPI_WIN_FLUSH_LOCAL
dev_langs:
- C++
- C
---

# MPI\_Win\_flush\_local function

Locally completes at the origin all outstanding RMA operations initiated by the calling process to the target process specified by rank on the specified window. For example, after this routine completes, the user may reuse any buffers provided to put, get, or accumulate operations.

## Syntax

``` c++
int MPIAPI MPI_Win_flush_local(
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
    MPI_WIN_FLUSH_LOCAL(RANK, WIN, IERROR)
        INTEGER RANK, WIN, IERROR
```

## Remarks

All flush and sync functions can be called only within passive target epochs.

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

