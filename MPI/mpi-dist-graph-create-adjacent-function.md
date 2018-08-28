---
title: MPI_Dist_graph_create_adjacent function
TOCTitle: MPI_Dist_graph_create_adjacent function
ms:assetid: 1E6FDB8C-6964-4DA4-837A-8DD4D304D48B
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt147723(v=VS.85)
ms:contentKeyID: 65803980
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_DIST_GRAPH_CREATE_ADJACENT
- mpif/MPI_Dist_graph_create_adjacent
- mpi/MPI_DIST_GRAPH_CREATE_ADJACENT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Dist_graph_create_adjacent
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

# MPI\_Dist\_graph\_create\_adjacent function

Returns a handle to a new communicator to which the distributed graph topology information is attached.

## Syntax

``` c++
int WINAPI MPI_Dist_graph_create_adjacent(
  _In_  MPI_Comm                comm_old,
        _In_range_(>=,0)  int   indegree,
        _In_reads_opt const int sources[],
        _In_reads_opt const int sourceweights[],
        _In_range_(>=,0)  int   outdegree,
        _In_reads_opt const int destinations[],
        _In_reads_opt const int destweights[],
  _In_  MPI_Info                info,
        _In_range_(0,1) int     reorder,
  _Out_ MPI_Comm                *comm_dist_graph
);
```

## Parameters

  - *comm\_old* \[in\]  
    The handle of the communicator without the topology information (handle).

  - *indegree*  
    Size of the *sources* and *sourceweights* arrays (non-negative integer).

  - *sources\[\]*  
    Ranks of processes for which the calling process is the destination (array of non-negative integers).

  - *sourceweights\[\]*  
    Weights of the corresponding edges into the calling process (array of non-negative integers).

  - *outdegree*  
    Size of the *destinations* and *destweights* arrays (non-negative integer).

  - *destinations\[\]*  
    Ranks of processes for which the calling process is the source (array of non-negative integers).

  - *destweights\[\]*  
    Weights of the corresponding edges out of the calling process (array of non-negative integers).

  - *info* \[in\]  
    Hints on optimization or interpretation of weights (handle). Currently use **MPI\_INFO\_NULL** as this variable is not being used internally.

  - *reorder*  
    Ranks may be reordered (true) or not (false) (logical). Currently this is not used internally.

  - *comm\_dist\_graph* \[out\]  
    Handle to the communicator with the distributed graph topology information attached (handle).

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_DIST_GRAPH_CREATE_ADJACENT (COMM_OLD, INDEGREE, SOURCES, SOURCEWEIGHTS,
    OUTDEGREE, DESTINATIONS, DESTWEIGHTS, INFO, REORDER,
    COMM_DIST_GRAPH, IERROR)
        INTEGER COMM_OLD, INDEGREE, SOURCES (*), SOURCEWEIGHTS (*), OUTDEGREE,
    DESTINATIONS (*), DESTWEIGHTS (*), INFO, COMM_DIST_GRAPH, IERROR
        LOGICAL REORDER

## Remarks

Each process in the *comm\_old* communicator passes all information about its incoming and outgoing edges in the virtual distributed graph topology. The calling processes must ensure that each edge of the graph is described in the source and in the destination process with the same weight, if the graph is weighted. If there are multiple edges for a given source-destination pair, then the sequence of the weights of these edges does not matter.

The complete communication topology is the combination of all edges shown in the sources array of all processes in *comm\_old*, which must be identical to the combination of all edges shown in the *destinations* array. Source and destination ranks must be process ranks of *comm\_old*. This allows a fully distributed specification of the communication graph. Isolated processes, that is, processes with no incoming or outgoing edges in the distributed topology, and thus have *indegree* or *outdegree* or both, as zero, are allowed.

The number of processes in the newly created communicator, *comm\_dist\_graph*, is identical to the number of processes in *comm\_old*. The call to this function is collective.

Weights are specified as non-negative integers using the *sourceweights* and *destweights* arrays, if the graph is a weighted graph. An application will need to specify **MPI\_UNWEIGHTED** for both the *sourceweights* and *destweights* arrays to indicate that all edges have the same (effectively no) weight. It is erroneous to supply **MPI\_UNWEIGHTED** for some but not all processes of *comm\_old*. The behavior in such a case is not guaranteed. If the graph is weighted, but *indegree* or *outdegree* is zero for a process, then **MPI\_WEIGHTS\_EMPTY** or any arbitrary array may be passed to *sourceweights* or *destweights* by that process.

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

[**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md)

[**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md)

[**MPI\_Dist\_graph\_neighbors**](mpi-dist-graph-neighbors-function.md)

