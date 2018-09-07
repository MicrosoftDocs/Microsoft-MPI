---
title: MPI_Wtick function
TOCTitle: MPI_Wtick function
ms:assetid: fa916c75-ea37-4ff2-a85e-975a726e5352
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520618(v=VS.85)
ms:contentKeyID: 59361089
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WTICK
- mpif/MPI_Wtick
- mpi/MPI_WTICK
dev_langs:
- C++
- C
---

# MPI\_Wtick function

Returns the resolution of [**MPI\_Wtime**](mpi-wtime-function.md).

## Syntax

``` c++
double MPIAPI MPI_Wtick(void);
```

## Parameters

This function has no parameters.

## Return value

Time in seconds of resolution of [**MPI\_Wtime**](mpi-wtime-function.md).

## Fortran

    DOUBLE PRECISION MPI_WTICK()

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

