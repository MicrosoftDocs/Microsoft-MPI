---
title: MPI_Dims_create function
TOCTitle: MPI_Dims_create function
ms:assetid: 8dd7b947-2842-4f6a-9d92-1b18e346b7af
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473292(v=VS.85)
ms:contentKeyID: 59360838
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_DIMS_CREATE
- mpif/MPI_Dims_create
- mpi/MPI_DIMS_CREATE
dev_langs:
- C++
- C
---

# MPI\_Dims\_create function

TBD

## Syntax

``` c++
int MPIAPI MPI_Dims_create(
   int                      nnodes,
   int                      ndims,
   _Inout_count_(ndims) int *dims
);
```

## Parameters

  - *nnodes*  
    TBD

  - *ndims*  
    TBD

  - *dims*  
    TBD

## Return value

TBD

## Fortran

    MPI_DIMS_CREATE(NNODES, NDIMS, DIMS, IERROR)
        INTEGER NNODES, NDIMS, DIMS(*), IERROR

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

[MPI Process Topology Functions](mpi-process-topology-functions.md)

