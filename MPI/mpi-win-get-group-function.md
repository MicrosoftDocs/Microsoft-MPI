---
title: MPI_Win_get_group function
TOCTitle: MPI_Win_get_group function
ms:assetid: bfab8339-31c4-4a46-87eb-fec77693d7c7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520607(v=VS.85)
ms:contentKeyID: 59361078
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_GET_GROUP
- mpif/MPI_Win_get_group
- mpi/MPI_WIN_GET_GROUP
dev_langs:
- C++
- C
---

# MPI\_Win\_get\_group function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_get_group(
        MPI_Win   win,
  _Out_ MPI_Group *group
);
```

## Parameters

  - *win*  
    TBD

  - *group* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_GET_GROUP(WIN, GROUP, IERROR)
        INTEGER WIN, GROUP, IERROR

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

