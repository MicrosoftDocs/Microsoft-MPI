---
title: MPI_Win_complete function
TOCTitle: MPI_Win_complete function
ms:assetid: b3d531e7-a108-4613-b3ad-7a1ada88bdbd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520594(v=VS.85)
ms:contentKeyID: 59361065
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_COMPLETE
- mpif/MPI_Win_complete
- mpi/MPI_WIN_COMPLETE
dev_langs:
- C++
- C
---

# MPI\_Win\_complete function

Completes all RMA operations initiated after an [**MPI\_Win\_start**](mpi-win-start-function.md).

## Syntax

``` c++
int MPIAPI MPI_Win_complete(
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
    MPI_WIN_COMPLETE(WIN, IERROR)
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

