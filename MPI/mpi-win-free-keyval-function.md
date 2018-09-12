---
title: MPI_Win_free_keyval function
TOCTitle: MPI_Win_free_keyval function
ms:assetid: 3fb0a67e-2aaa-4a33-9cb1-d6ee329219eb
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520604(v=VS.85)
ms:contentKeyID: 59361075
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FREE_KEYVAL
- mpif/MPI_Win_free_keyval
- mpi/MPI_WIN_FREE_KEYVAL
dev_langs:
- C++
- C
---

# MPI\_Win\_free\_keyval function

Frees an attribute key for MPI RMA windows.

## Syntax

``` c++
int MPIAPI MPI_Win_free_keyval(
  _Inout_  int *win_keyval
);
```

## Parameters

  - *win\_keyval* \[in, out\]  
    Key value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_FREE_KEYVAL(WIN_KEYVAL, IERROR)
        INTEGER WIN_KEYVAL, IERROR
```

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

[MPI Caching Functions](mpi-caching-functions.md)

