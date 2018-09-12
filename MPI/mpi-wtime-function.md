---
title: MPI_Wtime function
TOCTitle: MPI_Wtime function
ms:assetid: 089418b3-028b-4e5b-b94b-7aa3ef6891d4
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520619(v=VS.85)
ms:contentKeyID: 59361090
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WTIME
- mpif/MPI_Wtime
- mpi/MPI_WTIME
dev_langs:
- C++
- C
---

# MPI\_Wtime function

Returns an elapsed time on the calling processor.

## Syntax

``` c++
double MPIAPI MPI_Wtime(void);
```

## Parameters

This function has no parameters.

## Return value

Time in seconds since an arbitrary time in the past.

## Fortran

``` FORTRAN
    DOUBLE PRECISION MPI_WTIME()
```

## Remarks

This is intended to be a high-resolution, elapsed (or wall) clock. See [**MPI\_Wtick**](mpi-wtick-function.md) to determine the resolution of [**MPI\_Wtime**](mpi-wtime-function.md). If the attribute **MPI\_WTIME\_IS\_GLOBAL** is defined and true, then the value is synchronized across all processes in **MPI\_COMM\_WORLD**.

This is a function, declared as **DOUBLE PRECISION MPI\_WTIME()** in Fortran.

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

