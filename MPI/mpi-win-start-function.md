---
title: MPI_Win_start function
TOCTitle: MPI_Win_start function
ms:assetid: bf2616c8-c541-4f96-a0ae-2ab2401231b9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520614(v=VS.85)
ms:contentKeyID: 59361085
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_START
- mpif/MPI_Win_start
- mpi/MPI_WIN_START
dev_langs:
- C++
- C
---

# MPI\_Win\_start function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_start(
   MPI_Group group,
   int       assert,
   MPI_Win   win
);
```

## Parameters

  - *group*  
    TBD

  - *assert*  
    TBD

  - *win*  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_START(GROUP, ASSERT, WIN, IERROR)
        INTEGER GROUP, ASSERT, WIN, IERROR

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

