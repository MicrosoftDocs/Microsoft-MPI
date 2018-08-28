---
title: MPI_Startall function
TOCTitle: MPI_Startall function
ms:assetid: ffd68b75-c72e-4d48-aad8-103154f6bddc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473474(v=VS.85)
ms:contentKeyID: 59361009
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SSEND_INIT
- mpi/MPI_SSEND_INIT
- mpi/MPI_Startall
- MPI_Startall
- mpif/MPI_SSEND_INIT
- mpif/MPI_Startall
dev_langs:
- C++
- C
---

# MPI\_Startall function

TBD

## Syntax

``` c++
int MPIAPI MPI_Startall(
   int                              count,
   _Inout_count_(count) MPI_Request *array_of_requests
);
```

## Parameters

  - *count*  
    TBD

  - *array\_of\_requests*  
    TBD

## Return value

TBD

## Fortran

    MPI_STARTALL(COUNT, ARRAY_OF_REQUESTS, IERROR)
        INTEGER COUNT, ARRAY_OF_REQUESTS(*), IERROR

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

