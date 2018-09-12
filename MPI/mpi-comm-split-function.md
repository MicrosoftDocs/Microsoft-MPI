---
title: MPI_Comm_split function
TOCTitle: MPI_Comm_split function
ms:assetid: 32195e4e-b754-4766-9a38-9353854447e3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473286(v=VS.85)
ms:contentKeyID: 59360832
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SPLIT
- mpif/MPI_Comm_split
- mpi/MPI_COMM_SPLIT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_split
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

# MPI\_Comm\_split function

Partitions the group that is associated with the specified communicator into a specified number of disjoint subgroups.

## Syntax

``` c++
int MPIAPI MPI_Comm_split(
        MPI_Comm comm,
        int      color,
        int      key,
  _Out_ MPI_Comm *newcomm
);
```

## Parameters

  - *comm*  
    The communicator to split.

  - *color*  
    The new communicator that the calling process is to be assigned to. The value of *color* must be non-negative.
    
    If a process specifies the *color* value **MPI\_UNDEFINED**, the function returns **MPI\_COMM\_NULL** in the *newcomm* parameter to the calling process.

  - *key*  
    The relative rank of the calling process in the group of the new communicator. For details on using the *key* and *color* parameters, see Remarks.

  - *newcomm* \[out\]  
    On return, contains a handle to a new communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SPLIT(COMM,COLOR,KEY,NEWCOMM,IERROR)
        INTEGER COMM, COLOR, KEY, NEWCOMM, IERROR
```

## Remarks

This is a collective function, but each process can specify different values for the *color* and *key* parameters.

This is an extremely powerful mechanism for dividing a single communicating group of processes into an arbitrary number of subgroups. The number of subgroups is determined by the number of colors that are specified over all the processes. The resulting communicators do not overlap. Subdividing a communicator in this way is useful for defining a hierarchy of computations, such as for multigrid or linear algebra.

Each subgroup contains all the processes that specified the same value for the *color* parameter. Within each subgroup, the processes are ranked in the order that is defined by the value of the *key* parameter, with ties broken according to their rank in the old group.

With an intracommunicator communicator, a call to `MPI_COMM_CREATE(comm, group, new-comm)` is equivalent to a call to `MPI_COMM_SPLIT(comm, color, key, newcomm)`, where processes that are group members specify the number of the group, based on a unique numbering of all disjoint groups, for the *color* parameter and their rank in the group for the *key* parameter. All processes that are not members of the group specify **MPI\_UNDEFINED** for the *color* parameter.

For any one color, the key values do not have to be unique. The **MPI\_Comm\_split** function sorts processes in order according to the value of the *key* parameter, and it sorts ties by their relative rank in the source group. If the same value is specified for all the *key* parameters, then all the processes in a given color have the same relative rank order that they had in their parent group.

For intracommunicators, the **MPI\_Comm\_split** and [**MPI\_Comm\_create**](mpi-comm-create-function.md) functions provide similar capability to split a communicating group into disjoint subgroups.

The **MPI\_Comm\_split** function is used when some processes do not have complete information of the other members in their group, but all processes have the color of the group to which they belong. In this case, the MPI implementation discovers the other group members via communication.

The [**MPI\_Comm\_create**](mpi-comm-create-function.md) function is used when all processes have complete information of the members of their group. In this case, the MPI implementation can avoid the extra communication that is required to discover group membership.

Communicators created by **MPI\_Comm\_split** cannot overlap. You can call the **MPI\_Comm\_split** function multiple times to overcome this limitation. You can create multiple overlapping communication structures in this way. Creative use of the *color* and *key* parameters in such splitting operations is encouraged.

The result of the **MPI\_Comm\_split** function on an intercommunicator is that those processes on the left with the same color as those processes on the right combine to create a new intercommunicator. The *key* parameter defines the relative rank of processes on each side of the intercommunicator. A new communicator with a handle of **MPI\_COMM\_NULL** is returned to those processes that specify **MPI\_UNDEFINED** as their color, or specify a color that is only specified on one side of the intercommunicator.

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

[MPI Communicator Functions](mpi-communicator-functions.md)

[**MPI\_Comm\_create**](mpi-comm-create-function.md)

