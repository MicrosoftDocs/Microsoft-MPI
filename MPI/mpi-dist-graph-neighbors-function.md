---
title: MPI_Dist_graph_neighbors function
TOCTitle: MPI_Dist_graph_neighbors function
ms:assetid: 2C012D74-85CD-407F-B0B9-3B16D3FE6E0C
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt147724(v=VS.85)
ms:contentKeyID: 65803981
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_DIST_GRAPH_NEIGHBORS
- mpif/MPI_Dist_graph_neighbors
- mpi/MPI_DIST_GRAPH_NEIGHBORS
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Dist_graph_neighbors
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Dist_graph_neighbors function with this comprehensive guide. Learn about its syntax, parameters, return values, and how it works in a distributed graph topology.
---

# MPI\_Dist\_graph\_neighbors function

Returns the list of neighbors having edges into and out of the calling process, as well as the corresponding weights on the incoming and outgoing edges in a distributed graph topology.

## Syntax

``` c++
int WINAPI MPI_Dist_graph_neighbors(
  _In_ MPI_Comm              comm,
       _In_range_(>=,0)  int maxindegree,
       _Out_writes_opt int   sources[],
       _Out_writes_opt int   sourceweights[],
       _In_range_(>=,0)  int maxoutdegree,
       _Out_writes_opt int   destinations[],
       _Out_writes_opt int   destweights[]
);
```

## Parameters

  - *comm* \[in\]  
    The handle of the communicator with the distributed graph topology.

  - *maxindegree*  
    Size of the *sources* and *sourceweights* arrays (non-negative integer).

  - *sources\[\]*  
    Ranks of processes in the communicator for which, the calling process is the destination in the distributed graph topology (array of non-negative integers).

  - *sourceweights\[\]*  
    Weights of the corresponding edges into the calling process (array of non-negative integers).

  - *maxoutdegree*  
    Size of the *destinations* and *destweights* arrays (non-negative integer).

  - *destinations\[\]*  
    Ranks of processes in the communicator for which the calling process is the source in the distributed graph topology (array of non-negative integers).

  - *destweights\[\]*  
    Weights of the corresponding edges out of the calling process (array of non-negative integers).

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_DIST_GRAPH_NEIGHBORS (COMM, MAXINDEGREE, SOURCES, SOURCEWEIGHTS,
    MAXOUTDEGREE, DESTINATIONS, DESTWEIGHTS, IERROR)
        INTEGER COMM, MAXINDEGREE, SOURCES (*), SOURCEWEIGHTS (*), MAXOUTDEGREE,
    DESTINATIONS (*), DESTWEIGHTS (*), IERROR
```

## Remarks

The incoming and outgoing edge count and the weight information can be obtained by calling [**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md) prior to calling this method. If *maxindegree* and *maxoutdegree* are less than the number of incoming and outgoing edges returned by **MPI\_Dist\_graph\_neighbors\_count**, then only the first part of the full list is returned.

The incoming and outgoing edge weights are returned only if the graph was created as a weighted distributed graph by the [**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md) or the [**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md) methods and if **MPI\_UNWEIGHTED** is not supplied as an argument in place of *sourceweights* or *destweights*.

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md)

[**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md)

[**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md)

