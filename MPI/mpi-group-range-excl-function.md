---
title: MPI_Group_range_excl function
TOCTitle: MPI_Group_range_excl function
ms:assetid: 635a803a-a5a9-4d1c-a324-602048154f27
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473402(v=VS.85)
ms:contentKeyID: 59360938
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_RANGE_EXCL
- mpif/MPI_Group_range_excl
- mpi/MPI_GROUP_RANGE_EXCL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_range_excl
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to create a new group by removing processes from an existing one using the MPI_Group_range_excl function on Microsoft's official site.
---

# MPI\_Group\_range\_excl function

Creates a new group by removing processes from an existing group.

## Syntax

``` c++
int MPIAPI MPI_Group_range_excl(
        MPI_Group         group,
        int               n,
        _In_count_(n) int ranges[][3],
  _Out_ MPI_Group         *newgroup
);
```

## Parameters

  - *group*  
    The existing group.

  - *n*  
    The number of ranges of processes to exclude from the new group.

  - *ranges*  
    An array of specifications of processes to exclude from the existing group. Each element of the array specifies a range of process in the form of three integers for the first rank, last rank, and stride.

  - *newgroup* \[out\]  
    A pointer to a handle that represents the new group that contains those processes that were not excluded. The order of the group is preserved.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_RANGE_EXCL(GROUP, N, RANGES, NEWGROUP, IERROR)
        INTEGER GROUP, N, RANGES(3,*), NEWGROUP, IERROR
```

## Remarks

Each computed rank must be a valid rank in the existing group and all computed ranks must be distinct; otherwise the function returns an error.

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

[**MPI\_Group\_excl**](mpi-group-excl-function.md)

[**MPI\_Comm\_group**](mpi-comm-group-function.md)

