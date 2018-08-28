---
title: MPI_Graph_map function
TOCTitle: MPI_Graph_map function
ms:assetid: 43f34f5d-dd31-4173-b441-4c330fe7f75e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473387(v=VS.85)
ms:contentKeyID: 59360923
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPH_MAP
- mpif/MPI_Graph_map
- mpi/MPI_GRAPH_MAP
dev_langs:
- C++
- C
---

# MPI\_Graph\_map function

TBD

## Syntax

``` c++
int MPIAPI MPI_Graph_map(
        MPI_Comm               comm,
        int                    nnodes,
        _In_count_(nnodes) int *index,
  _In_  int                    *edges,
  _Out_ int                    *newrank
);
```

## Parameters

  - *comm*  
    TBD

  - *nnodes*  
    TBD

  - *index*  
    TBD

  - *edges* \[in\]  
    TBD

  - *newrank* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_GRAPH_MAP(COMM, NNODES, INDEX, EDGES, NEWRANK, IERROR)
        INTEGER COMM, NNODES, INDEX(*), EDGES(*), NEWRANK, IERROR

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

