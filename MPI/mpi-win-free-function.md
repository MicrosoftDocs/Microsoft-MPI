---
title: MPI_Win_free function
TOCTitle: MPI_Win_free function
ms:assetid: daa35d13-e417-4159-99fb-ff9f9605df11
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520603(v=VS.85)
ms:contentKeyID: 59361074
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FREE
- mpif/MPI_Win_free
- mpi/MPI_WIN_FREE
dev_langs:
- C++
- C
description: Explore the MPI_Win_free function on Microsoft's learning platform. Understand its syntax, parameters, return values, and application in Fortran.
---

# MPI\_Win\_free function

Frees an MPI window object.

## Syntax

``` c++
int MPIAPI MPI_Win_free(
  _Inout_ MPI_Win *win
);
```

## Parameters

  - *win* \[in, out\]  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_FREE(WIN, IERROR)
        INTEGER WIN, IERROR
```

## Remarks

If successfully freed, *win* is set to **MPI\_WIN\_NULL**.

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

