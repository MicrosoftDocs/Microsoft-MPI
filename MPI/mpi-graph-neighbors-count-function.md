---
title: MPI_Graph_neighbors_count function
TOCTitle: MPI_Graph_neighbors_count function
ms:assetid: f2d8fdf3-1487-4301-9519-191f21af68c2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473389(v=VS.85)
ms:contentKeyID: 59360925
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPH_NEIGHBORS_COUNT
- mpif/MPI_Graph_neighbors_count
- mpi/MPI_GRAPH_NEIGHBORS_COUNT
dev_langs:
- C++
- C
---

# MPI\_Graph\_neighbors\_count function

TBD

## Syntax

``` c++
int MPIAPI MPI_Graph_neighbors_count(
        MPI_Comm comm,
        int      rank,
  _Out_ int      *nneighbors
);
```

## Parameters

  - *comm*  
    TBD

  - *rank*  
    TBD

  - *nneighbors* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_GRAPH_NEIGHBORS_COUNT(COMM, RANK, NNEIGHBORS, IERROR)
        INTEGER COMM, RANK, NNEIGHBORS, IERROR

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

