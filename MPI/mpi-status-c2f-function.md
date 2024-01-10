---
title: MPI_Status_c2f function
TOCTitle: MPI_Status_c2f function
ms:assetid: 2bb2d54f-b801-41a7-a1db-4d792858cc2c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473476(v=VS.85)
ms:contentKeyID: 59361011
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Status_c2f
- MPI_Status_c2f
- mpif/MPI_Status_c2f
dev_langs:
- C++
- C
---

# MPI\_Status\_c2f function

Converts from a C status (which is a structure) to a Fortran status (which is an array of integers).

## Syntax

``` c++
int MPIAPI MPI_Status_c2f(
  _In_  MPI_Status *status,
  _Out_ MPI_Fint   *f_status
);
```

## Parameters

  - *status* \[in\]  
    C status.

  - *f\_status* \[out\]  
    Fortran status.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

