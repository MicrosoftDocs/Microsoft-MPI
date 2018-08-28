---
title: MPI_Status_f2c function
TOCTitle: MPI_Status_f2c function
ms:assetid: 427308ed-2fb0-411e-bab5-d3e78ad35dcd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473477(v=VS.85)
ms:contentKeyID: 59361012
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Status_f2c
- MPI_Status_f2c
- mpif/MPI_Status_f2c
dev_langs:
- C++
- C
---

# MPI\_Status\_f2c function

TBD

## Syntax

``` c++
int MPIAPI MPI_Status_f2c(
  _In_  MPI_Fint   *f_status,
  _Out_ MPI_Status *status
);
```

## Parameters

  - *f\_status* \[in\]  
    TBD

  - *status* \[out\]  
    TBD

## Return value

TBD

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

