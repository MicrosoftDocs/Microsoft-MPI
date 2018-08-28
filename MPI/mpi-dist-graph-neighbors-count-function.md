---
title: MPI_Dist_graph_neighbors_count function
TOCTitle: MPI_Dist_graph_neighbors_count function
ms:assetid: 1016274C-C079-4770-962E-8036FF696B71
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt147725(v=VS.85)
ms:contentKeyID: 65803982
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_DIST_GRAPH_NEIGHBORS_COUNT
- mpif/MPI_Dist_graph_neighbors_count
- mpi/MPI_DIST_GRAPH_NEIGHBORS_COUNT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Dist_graph_neighbors_count
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Dist\_graph\_neighbors\_count function

Obtains adjacency information of the calling process in a distributed graph topology. The information that is obtained by this function, on the number of incoming edges, outgoing edges, and a flag indicating if the distributed graph is weighted, matches the information provided in the call to [**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md) or [**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md) (by the calling process in the case of **MPI\_Dist\_graph\_create\_adjacent**, or potentially by processes other than the calling process in the case of **MPI\_Dist\_graph\_create**).

## Syntax

``` c++
int WINAPI MPI_Dist_graph_neighbors_count(
  _In_  MPI_Comm comm,
  _Out_ int      indegree,
  _Out_ int      outdegree,
  _Out_ int      weighted
);
```

## Parameters

  - *comm* \[in\]  
    The handle of the communicator with the distributed graph topology.

  - *indegree* \[out\]  
    Number of edges into this process (non-negative integer).

  - *outdegree* \[out\]  
    Number of edges out of this process (non-negative integer).

  - *weighted* \[out\]  
    Is false if **MPI\_UNWEIGHTED** was supplied during creation, true otherwise.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_DIST_GRAPH_NEIGHBORS_COUNT (COMM, INDEGREE, OUTDEGREE, WEIGHTED, IERROR)
        INTEGER COMM, INDEGREE, OUTDEGREE, IERROR
        LOGICAL WEIGHTED

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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

[**MPI\_Dist\_graph\_neighbors**](mpi-dist-graph-neighbors-count-function.md)

[**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md)

[**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md)

