---
title: MPI_Graph_get function
TOCTitle: MPI_Graph_get function
ms:assetid: dc024019-391a-41d4-b3eb-10a8d38b984d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473386(v=VS.85)
ms:contentKeyID: 59360922
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPH_GET
- mpif/MPI_Graph_get
- mpi/MPI_GRAPH_GET
dev_langs:
- C++
- C
---

# MPI\_Graph\_get function

Retrieves graph topology information associated with a communicator.

## Syntax

``` c++
int MPIAPI MPI_Graph_get(
   MPI_Comm                comm,
   int                     maxindex,
   int                     maxedges,
   _Out_cap_(maxindex) int *index,
   _Out_cap_(maxindex) int *edges
);
```

## Parameters

  - *comm*  
    Communicator with graph structure.

  - *maxindex*  
    Length of the *index* vector in the calling program.

  - *maxedges*  
    Length of the *edges* vector in the calling program.

  - *index*  
    Array of integers containing the graph structure.

  - *edges*  
    Array of integers containing the graph structure.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GRAPH_GET(COMM, MAXINDEX, MAXEDGES, INDEX, EDGES, IERROR)
        INTEGER COMM, MAXINDEX, MAXEDGES, INDEX(*), EDGES(*), IERROR
```

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

