---
title: MPI_Graph_create function
TOCTitle: MPI_Graph_create function
ms:assetid: e77ff296-4803-41a6-8c53-d758022cab5b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473385(v=VS.85)
ms:contentKeyID: 59360921
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPH_CREATE
- mpif/MPI_Graph_create
- mpi/MPI_GRAPH_CREATE
dev_langs:
- C++
- C
---

# MPI\_Graph\_create function

TBD

## Syntax

``` c++
int MPIAPI MPI_Graph_create(
        MPI_Comm               comm_old,
        int                    nnodes,
        _In_count_(nnodes) int *index,
  _In_  int                    *edges,
        int                    reorder,
  _Out_ MPI_Comm               *comm_cart
);
```

## Parameters

  - *comm\_old*  
    TBD

  - *nnodes*  
    TBD

  - *index*  
    TBD

  - *edges* \[in\]  
    TBD

  - *reorder*  
    TBD

  - *comm\_cart* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_GRAPH_CREATE(COMM_OLD, NNODES, INDEX, EDGES, REORDER, COMM_GRAPH, IERROR)
        INTEGER COMM_OLD, NNODES, INDEX(*), EDGES(*), COMM_GRAPH, IERROR
        LOGICAL REORDER

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

