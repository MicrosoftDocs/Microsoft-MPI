---
title: MPI Process Topology Functions
TOCTitle: MPI Process Topology Functions
ms:assetid: EF52087F-9343-40C3-BAEE-6F1F9B9F9C85
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473449(v=VS.85)
ms:contentKeyID: 59360984
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Process Topology Functions

## In this section

  - [**MPI\_Cart\_coords**](mpi-cart-coords-function.md)  
    Determines process coords in cartesian topology given rank in group.

  - [**MPI\_Cart\_create**](mpi-cart-create-function.md)  
    Makes a new communicator to which topology information is being attached.

  - [**MPI\_Cart\_get**](mpi-cart-get-function.md)  
    Retrieves cartesian topology information associated with a communicator.

  - [**MPI\_Cart\_map**](mpi-cart-map-function.md)  
    Maps process to cartesian topology information.

  - [**MPI\_Cart\_rank**](mpi-cart-rank-function.md)  
    Determines process rank in communicator by its cartesian location.

  - [**MPI\_Cart\_shift**](mpi-cart-shift-function.md)  
    Returns the shifted source and destination ranks, given a shift direction and amount.

  - [**MPI\_Cart\_sub**](mpi-cart-sub-function.md)  
    Partitions a communicator into subgroups that form lower-dimensional cartesian subgrids.

  - [**MPI\_Cartdim\_get**](mpi-cartdim-get-function.md)  
    Retrieves cartesian topology information associated with a communicator.

  - [**MPI\_Dims\_create**](mpi-dims-create-function.md)  
    Creates a division of processors in a cartesian grid.

  - [**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md)  
    Returns a handle to a new communicator to which the distributed graph topology information is attached.

  - [**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md)  
    Returns a handle to a new communicator to which the distributed graph topology information is attached.

  - [**MPI\_Dist\_graph\_neighbors**](mpi-dist-graph-neighbors-function.md)  
    Returns the list of neighbors having edges into and out of the calling process, as well as the corresponding weights on the incoming and outgoing edges in a distributed graph topology.

  - [**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md)  
    Obtains adjacency information of the calling process in a distributed graph topology. The information that is obtained by this function, on the number of incoming edges, outgoing edges, and a flag indicating if the distributed graph is weighted, matches the information provided in the call to [**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md) or [**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md) (by the calling process in the case of **MPI\_Dist\_graph\_create\_adjacent**, or potentially by processes other than the calling process in the case of **MPI\_Dist\_graph\_create**).

  - [**MPI\_Graph\_create**](mpi-graph-create-function.md)  
    Makes a new communicator to which topology information is being attached.

  - [**MPI\_Graph\_get**](mpi-graph-get-function.md)  
    Retrieves graph topology information associated with a communicator.

  - [**MPI\_Graph\_map**](mpi-graph-map-function.md)  
    Maps process to graph topology information.

  - [**MPI\_Graph\_neighbors**](mpi-graph-neighbors-function.md)  
    Returns the neighbors of a node associated with a graph topology.

  - [**MPI\_Graph\_neighbors\_count**](mpi-graph-neighbors-count-function.md)  
    Returns the number of neighbors of a node associated with a graph topology.

  - [**MPI\_Graphdims\_get**](mpi-graphdims-get-function.md)  
    Retrieves graph topology information associated with a communicator.

