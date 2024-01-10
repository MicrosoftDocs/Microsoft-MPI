---
title: MPI_Group_excl function
TOCTitle: MPI_Group_excl function
ms:assetid: d5b17422-4ff1-4c64-ba0e-72d8365f066b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473397(v=VS.85)
ms:contentKeyID: 59360933
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_EXCL
- mpif/MPI_Group_excl
- mpi/MPI_GROUP_EXCL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_excl
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Group_excl function to define a new group by deleting ranks from an existing group on Microsoft's official site.
---

# MPI\_Group\_excl function

A group constructor that is used to define a new group by deleting ranks from an existing group.

## Syntax

``` c++
int MPIAPI MPI_Group_excl(
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
    The number of elements in the *ranks* parameter.

  - *ranks*  
    The arrays of processes in *group* that are not to appear in *newgroup*. The specified ranks must be valid in the existing group. Each element in the array must be distinct. If the array is empty then the new group will be identical to the existing group.

  - *newgroup* \[out\]  
    A pointer to a handle that represents the new group that is derived from the existing group. The order of the existing group is preserved in the new group.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_EXCL(GROUP, N, RANKS, NEWGROUP, IERROR)
        INTEGER GROUP, N, RANKS(*), NEWGROUP, IERROR
```

## Remarks

This function creates a new group of processes that is derived by removing specified processes from an existing group while preserving the order of the ranks in the group.

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

