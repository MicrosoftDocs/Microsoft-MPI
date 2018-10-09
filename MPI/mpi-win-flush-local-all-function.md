---
title: MPI_Win_flush_local_all function
TOCTitle: MPI_Win_flush_local_all function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FLUSH_LOCAL_ALL
- mpif/MPI_Win_flush_local_all
- mpi/MPI_WIN_FLUSH_LOCAL_ALL
dev_langs:
- C++
- C
---

# MPI\_Win\_flush\_local\_all function

All RMA operations issued to any target prior to this call in this window will have completed at the origin when this call returns.

## Syntax

``` c++
int MPIAPI MPI_Win_flush_local_all(
        MPI_Win  *win
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
    MPI_WIN_FLUSH_LOCAL_ALL(WIN, IERROR)
        INTEGER WIN, IERROR
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

