---
title: MPI_Dist_graph_create function
TOCTitle: MPI_Dist_graph_create function
ms:assetid: AA8B083C-E601-4E64-BAEE-09CB364A005F
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt147722(v=VS.85)
ms:contentKeyID: 65803979
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_DIST_GRAPH_CREATE
- mpif/MPI_Dist_graph_create
- mpi/MPI_DIST_GRAPH_CREATE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Dist_graph_create
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

# MPI\_Dist\_graph\_create function

Returns a handle to a new communicator to which the distributed graph topology information is attached.

## Syntax

``` c++
int WINAPI MPI_Dist_graph_create(
  _In_  MPI_Comm                comm_old,
        _In_range_(>=,0)  int   n,
        _In_reads_opt const int sources[],
        _In_reads_opt const int degrees[],
        _In_opt const int       destinations[],
        _In_opt const int       weights[],
  _In_  MPI_Info                info,
        _In_range_(0,1) int     reorder,
  _Out_ MPI_Comm                *comm_dist_graph
);
```

## Parameters

  - *comm\_old* \[in\]  
    The handle of the communicator without the topology information (handle).

  - *n*  
    Number of sources for which this process specifies outgoing edges (non-negative integer).

  - *sources\[\]*  
    Array containing the *n* sources for which this source specifies the outgoing edges (array of non-negative integers).

  - *degrees\[\]*  
    Array specifying the number of destinations for each source node in the source node array (array of non-negative integers).

  - *destinations\[\]*  
    Destination nodes for the source nodes in the sources array (array of non-negative integers).

  - *weights\[\]*  
    Weights for corresponding edges in the *destinations* array (array of non-negative integers).

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

    MPI_DIST_GRAPH_CREATE (COMM_OLD, N, SOURCES, DEGREES, DESTINATIONS, WEIGHTS,
    INFO, REORDER, COMM_DIST_GRAPH, IERROR)
        INTEGER COMM_OLD, N, SOURCES (*), DEGREES (*), DESTINATIONS (*),
    WEIGHTS (*), INFO, COMM_DIST_GRAPH, IERROR
        LOGICAL REORDER

## Remarks

Both the *sources* and *destinations* arrays may contain the same node more than once, and the order in which nodes are listed as destinations or sources is not significant. Similarly, different processes may specify edges with the same source and destination nodes. Source and destination nodes must be process ranks of *comm\_old*. Different processes may specify different numbers of source and destination nodes, as well as different source to destination edges. This allows a fully distributed specification of the communication graph. Isolated processes (processes with no outgoing or incoming edges, that is, processes that do not occur as source or destination node in the graph specification) are allowed.

The number of processes in *comm\_dist\_graph* is identical to the number of processes in *comm\_old*. The call to this function is collective.

In C or FORTRAN, an application can supply **MPI\_UNWEIGHTED** for the *weights* array to indicate that all edges have the same (effectively no) weight. It is erroneous to supply **MPI\_UNWEIGHTED** for some but not all processes of *comm\_old*. The behavior in such a case is not guaranteed. If the graph is weighted, but *n* = 0, then, **MPI\_WEIGHTS\_EMPTY** or any arbitrary array may be passed to *weights*.

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

[**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md)

[**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md)

[**MPI\_Dist\_graph\_neighbors**](mpi-dist-graph-neighbors-function.md)

