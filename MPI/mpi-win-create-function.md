---
title: MPI_Win_create function
TOCTitle: MPI_Win_create function
ms:assetid: fccf3c21-8840-4de4-8d97-e8bb778771e2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520596(v=VS.85)
ms:contentKeyID: 59361067
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CREATE
- mpif/MPI_Win_create
- mpi/MPI_WIN_CREATE
dev_langs:
- C++
- C
---

# MPI\_Win\_create function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_create(
  _In_  void     *base,
        MPI_Aint size,
        int      disp_unit,
        MPI_Info info,
        MPI_Comm comm,
  _Out_ MPI_Win  *win
);
```

## Parameters

  - *base* \[in\]  
    TBD

  - *size*  
    TBD

  - *disp\_unit*  
    TBD

  - *info*  
    TBD

  - *comm*  
    TBD

  - *win* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_CREATE(BASE, SIZE, DISP_UNIT, INFO, COMM, WIN, IERROR)
        <type> BASE(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
        INTEGER DISP_UNIT, INFO, COMM, WIN, IERROR

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

