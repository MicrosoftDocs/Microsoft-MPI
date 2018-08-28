---
title: MPI_Win_post function
TOCTitle: MPI_Win_post function
ms:assetid: 7bc39c36-ca44-455b-9232-288036278612
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520610(v=VS.85)
ms:contentKeyID: 59361081
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_POST
- mpif/MPI_Win_post
- mpi/MPI_WIN_POST
dev_langs:
- C++
- C
---

# MPI\_Win\_post function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_post(
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

    MPI_WIN_POST(GROUP, ASSERT, WIN, IERROR)
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

