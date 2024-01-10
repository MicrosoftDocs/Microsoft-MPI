---
title: MPI_Group_intersection function
TOCTitle: MPI_Group_intersection function
ms:assetid: 06b3f54f-5260-49f6-a5f1-81358daa5413
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473401(v=VS.85)
ms:contentKeyID: 59360937
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_INTERSECTION
- mpif/MPI_Group_intersection
- mpi/MPI_GROUP_INTERSECTION
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_intersection
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: "Discover MPI Group Intersection Function: create new groups from existing ones with Microsoft's Message Passing Interface. Learn more now."
---

# MPI\_Group\_intersection function

Creates a new group from the intersection of two existing groups.

## Syntax

``` c++
int MPIAPI MPI_Group_intersection(
        MPI_Group group1,
        MPI_Group group2,
  _Out_ MPI_Group *newgroup
);
```

## Parameters

  - *group1*  
    The first group.

  - *group2*  
    The second group.

  - *newgroup* \[out\]  
    A pointer to a handle that represents a new group with those elements that are present in both groups. The function returns **MPI\_GROUP\_EMPTY** if the new group is empty.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_INTERSECTION(GROUP1, GROUP2, NEWGROUP, IERROR)
        INTEGER GROUP1, GROUP2, NEWGROUP, IERROR 
```

## Remarks

This is a local operation. Different processes can define distinct groups. A process can define a group that does not include itself.

The MPI implementation does not provide a mechanism to build a group from scratch, but only from existing groups. The base group, upon which all other groups are defined, can be retrieved by using the [**MPI\_Comm\_group**](mpi-comm-group-function.md) function. It is the group that is associated with the initial communicator **MPI\_COMM\_WORLD**.

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

[MPI Group Functions](mpi-group-functions.md)

[**MPI\_Comm\_group**](mpi-comm-group-function.md)

