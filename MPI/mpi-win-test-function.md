---
title: MPI_Win_test function
TOCTitle: MPI_Win_test function
ms:assetid: d43eee70-534a-4f0f-a5cd-fb442a809fe2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520615(v=VS.85)
ms:contentKeyID: 59361086
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_TEST
- mpif/MPI_Win_test
- mpi/MPI_WIN_TEST
dev_langs:
- C++
- C
---

# MPI\_Win\_test function

TBD

## Syntax

``` c++
int MPIAPI MPI_Win_test(
        MPI_Win win,
  _Out_ int     *flag
);
```

## Parameters

  - *win*  
    TBD

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_WIN_TEST(WIN, FLAG, IERROR)
        INTEGER WIN, IERROR
        LOGICAL FLAG

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

