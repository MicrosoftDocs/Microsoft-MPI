---
title: MPI_Group_incl function
TOCTitle: MPI_Group_incl function
ms:assetid: 59def9d7-933a-43e2-8218-1bf874b786da
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473400(v=VS.85)
ms:contentKeyID: 59360936
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_INCL
- mpif/MPI_Group_incl
- mpi/MPI_GROUP_INCL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_incl
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to create a new group with a subset of processes using the MPI_Group_incl function on Microsoft's official site.
---

# MPI\_Group\_incl function

Creates a new group that contains a subset of the processes in an existing group.

## Syntax

``` c++
int MPIAPI MPI_Group_incl(
        MPI_Group         group,
        int               n,
        _In_count_(n) int *ranks,
  _Out_ MPI_Group         *newgroup
);
```

## Parameters

  - *group*  
    The existing group.

  - *n*  
    The number of elements in the *ranks* parameter and the size of the new group.

  - *ranks*  
    The processes to be included in the new group.

  - *newgroup* \[out\]  
    A pointer to a handle that represents the new group, which contains the included processes in the order that they are specified in the *ranks* parameter.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_INCL(GROUP, N, RANKS, NEWGROUP, IERROR)
        INTEGER GROUP, N, RANKS(*), NEWGROUP, IERROR
```

## Remarks

This function can be used to reorder the elements of a group.

This is a local operation. Different processes can define distinct groups. A process can define a group that does not include itself.

The MPI implementation does not provide a mechanism to build a group from scratch, but only from existing groups. The base group, upon which all other groups are defined, can be retrieved by using the [**MPI\_Comm\_group**](mpi-comm-group-function.md) function. It is the group that is associated with the initial communicator **MPI\_COMM\_WORLD**.

## Requirements

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HHPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
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

[MPI Group Functions](mpi-group-functions.md)

[**MPI\_Comm\_group**](mpi-comm-group-function.md)

