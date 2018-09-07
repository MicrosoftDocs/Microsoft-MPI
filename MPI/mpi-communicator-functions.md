---
title: MPI Communicator Functions
TOCTitle: MPI Communicator Functions
ms:assetid: EF7FD722-0ACF-4297-BEF1-CFD0F569DE8D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473255(v=VS.85)
ms:contentKeyID: 59360801
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Communicator Functions

## In this section

  - [**MPI\_Comm\_compare**](mpi-comm-compare-function.md)  
    Compares two communicator handles.

  - [**MPI\_Comm\_create**](mpi-comm-create-function.md)  
    Extracts a subset a group of processes for the purpose of separate Multiple Instruction Multiple Data (MIMD) computation in a separate communicator.

  - [**MPI\_Comm\_dup**](mpi-comm-dup-function.md)  
    Duplicates an existing communicator with associated key values.

  - [**MPI\_Comm\_free**](mpi-comm-free-function.md)  
    Frees a communicator that is allocated with the [**MPI\_Comm\_dup**](mpi-comm-dup-function.md), [**MPI\_Comm\_create**](mpi-comm-create-function.md), or [**MPI\_Comm\_split**](mpi-comm-split-function.md) functions.

  - [**MPI\_Comm\_rank**](mpi-comm-rank-function.md)  
    Retrieves the rank of the calling process in the group of the specified communicator.

  - [**MPI\_Comm\_size**](mpi-comm-size-function.md)  
    Retrieves the number of processes involved in a communicator, or the total number of processes available.

  - [**MPI\_Comm\_split**](mpi-comm-split-function.md)  
    Partitions the group that is associated with the specified communicator into a specified number of disjoint subgroups.

  - [**MPI\_Comm\_remote\_group**](mpi-comm-remote-group-function.md)  
    Accesses the remote group associated with the given inter-communicator.

  - [**MPI\_Comm\_remote\_size**](mpi-comm-remote-size-function.md)  
    Determines the size of the remote group associated with an inter-communictor.

  - [**MPI\_Comm\_test\_inter**](mpi-comm-test-inter-function.md)  
    Tests to see if a comm is an inter-communicator.

  - [**MPI\_Intercomm\_create**](mpi-intercomm-create-function.md)  
    Creates an intercommuncator from two intracommunicators.

  - [**MPI\_Intercomm\_merge**](mpi-intercomm-merge-function.md)  
    Creates an intracommuncator from an intercommunicator.

