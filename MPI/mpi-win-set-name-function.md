---
title: MPI_Win_set_name function
TOCTitle: MPI_Win_set_name function
ms:assetid: 0296ec58-73e0-49ad-bd4e-bc1bf0afffe2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520613(v=VS.85)
ms:contentKeyID: 59361084
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_SET_NAME
- mpif/MPI_Win_set_name
- mpi/MPI_WIN_SET_NAME
dev_langs:
- C++
- C
---

# MPI\_Win\_set\_name function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_set_name(
       MPI_Win win,
  _In_ char    *win_name
);
```

## Parameters

  - *win*  
    TBD

  - *win\_name* \[in\]  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_SET_NAME(WIN, WIN_NAME, IERROR)
        INTEGER WIN, IERROR
        CHARACTER*(*) WIN_NAME

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

