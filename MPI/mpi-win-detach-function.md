---
title: MPI_Win_detach function
TOCTitle: MPI_Win_detach function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_DETACH
- mpif/MPI_Win_detach
- mpi/MPI_WIN_DETACH
dev_langs:
- C++
- C
---

# MPI\_Win\_detach function

Detaches a previously attached memory region.

## Syntax

``` c++
int MPIAPI MPI_Win_detach(
   MPI_Win  win,
   void*    base
);
```

## Parameters

  - *win* \[in\]  
    Window object.

  - *base* \[in\]  
    Initial address of memory to be detached.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_DETACH(WIN, BASE, IERROR)
        INTEGER WIN, IERROR
        <type> BASE(*)
```

## Remarks

The arguments *base* and *win* must match the arguments passed to a previous call to [**MPI\_Win\_attach**](mpi-win-attach-function.md).

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

