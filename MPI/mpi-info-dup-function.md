---
title: MPI_Info_dup function
TOCTitle: MPI_Info_dup function
ms:assetid: 99d49571-e529-475c-85fb-fca63cc3e19a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473411(v=VS.85)
ms:contentKeyID: 59360947
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_DUP
- mpif/MPI_Info_dup
- mpi/MPI_INFO_DUP
dev_langs:
- C++
- C
---

# MPI\_Info\_dup function

TBD

## Syntax

``` c++
int MPIAPI MPI_Info_dup(
        MPI_Info info,
  _Out_ MPI_Info *newinfo
);
```

## Parameters

  - *info*  
    TBD

  - *newinfo* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_INFO_DUP(INFO, NEWINFO, IERROR)
        INTEGER INFO, NEWINFO, IERROR

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

[MPI Info Object Functions](mpi-info-object-functions.md)

