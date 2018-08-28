---
title: MPI_Graph_neighbors function
TOCTitle: MPI_Graph_neighbors function
ms:assetid: 19dc31c9-f9c8-4643-b4ca-8a717d9cc745
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473388(v=VS.85)
ms:contentKeyID: 59360924
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPH_NEIGHBORS
- mpif/MPI_Graph_neighbors
- mpi/MPI_GRAPH_NEIGHBORS
dev_langs:
- C++
- C
---

# MPI\_Graph\_neighbors function

TBD

## Syntax

``` c++
int MPIAPI MPI_Graph_neighbors(
   MPI_Comm                    comm,
   int                         rank,
   int                         maxneighbors,
   _Out_cap_(maxneighbors) int *neighbors
);
```

## Parameters

  - *comm*  
    TBD

  - *rank*  
    TBD

  - *maxneighbors*  
    TBD

  - *neighbors*  
    TBD

## Return value

TBD

## Fortran

    MPI_GRAPH_NEIGHBORS(COMM, RANK, MAXNEIGHBORS, NEIGHBORS, IERROR)
        INTEGER COMM, RANK, MAXNEIGHBORS, NEIGHBORS(*), IERROR

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

