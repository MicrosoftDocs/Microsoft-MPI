---
title: MPI_Win_sync function
TOCTitle: MPI_Win_sync function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_SYNC
- mpif/MPI_Win_sync
- mpi/MPI_WIN_SYNC
dev_langs:
- C++
- C
---

# MPI\_Win\_sync function

Synchronizes the private and public window copies of win.

## Syntax

``` c++
int MPIAPI MPI_Win_sync(
  _Inout_ MPI_Win *win
);
```

## Parameters

  - *win* \[in\]  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_SYNC(WIN, IERROR)
        INTEGER WIN, IERROR
```

## Remarks

For the purposes of synchronizing the private and public window, [**MPI\_Win\_sync**](mpi-win-sync-function.md) has the effect of ending and reopening an access and exposure epoch on the window (note that it does not actually end an epoch or complete any pending MPI RMA operations).

Microsoft MPI uses unified memory model, and so doesn't utilize private and public copies of the window memory. 

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

