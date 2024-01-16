---
title: MPI_Graphdims_get function
TOCTitle: MPI_Graphdims_get function
ms:assetid: ef8b9432-ac5a-42c3-ac0b-03891d789414
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473384(v=VS.85)
ms:contentKeyID: 59360920
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GRAPHDIMS_GET
- mpif/MPI_Graphdims_get
- mpi/MPI_GRAPHDIMS_GET
dev_langs:
- C++
- C
description: Learn about MPI_Graphdims_get function on Microsoft's site. It retrieves graph topology info associated with a communicator. Perfect for HPC Pack users.
---

# MPI\_Graphdims\_get function

Retrieves graph topology information associated with a communicator.

## Syntax

``` c++
int MPIAPI MPI_Graphdims_get(
        MPI_Comm comm,
  _Out_ int      *nnodes,
  _Out_ int      *nedges
);
```

## Parameters

  - *comm*  
    Communicator for group with graph structure.

  - *nnodes* \[out\]  
    Number of nodes in graph.

  - *nedges* \[out\]  
    Number of edges in graph.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GRAPHDIMS_GET(COMM, NNODES, NEDGES, IERROR)
        INTEGER COMM, NNODES, NEDGES, IERROR
```

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

