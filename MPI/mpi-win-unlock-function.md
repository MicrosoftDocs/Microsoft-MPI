---
title: MPI_Win_unlock function
TOCTitle: MPI_Win_unlock function
ms:assetid: 1fda2d0f-1b14-4b06-890c-3eba478d438c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520616(v=VS.85)
ms:contentKeyID: 59361087
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_UNLOCK
- mpif/MPI_Win_unlock
- mpi/MPI_WIN_UNLOCK
dev_langs:
- C++
- C
---

# MPI\_Win\_unlock function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_unlock(
   int     rank,
   MPI_Win win
);
```

## Parameters

  - *rank*  
    TBD

  - *win*  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_UNLOCK(RANK, WIN, IERROR)
        INTEGER RANK, WIN, IERROR

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

