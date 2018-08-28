---
title: MPI_Win_get_errhandler function
TOCTitle: MPI_Win_get_errhandler function
ms:assetid: dd5cd778-3db5-4d14-b08a-6f8eb23d4113
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520606(v=VS.85)
ms:contentKeyID: 59361077
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_GET_ERRHANDLER
- mpif/MPI_Win_get_errhandler
- mpi/MPI_WIN_GET_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Win\_get\_errhandler function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_get_errhandler(
        MPI_Win        win,
  _Out_ MPI_Errhandler *errhandler
);
```

## Parameters

  - *win*  
    TBD

  - *errhandler* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_GET_ERRHANDLER(WIN, ERRHANDLER, IERROR)
        INTEGER WIN, ERRHANDLER, IERROR

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

[MPI Management Functions](mpi-management-functions.md)

