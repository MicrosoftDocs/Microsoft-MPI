---
title: MPI_Group_range_incl function
TOCTitle: MPI_Group_range_incl function
ms:assetid: c6e95b30-78ad-45a2-adcc-78cf343c8681
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473403(v=VS.85)
ms:contentKeyID: 59360939
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_RANGE_INCL
- mpif/MPI_Group_range_incl
- mpi/MPI_GROUP_RANGE_INCL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_range_incl
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to define a new group using the MPI_Group_range_incl function on Microsoft's platform. Understand syntax, parameters, and return values.
---

# MPI\_Group\_range\_incl function

A group constructor that is used to define a new group by adding additional sets of ranks to an existing group.

## Syntax

``` c++
int MPIAPI MPI_Group_range_incl(
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
    The number of triplets in array ranges.

  - *ranges*  
    An array of specifications of processes to include in the new group. Each element of the array specifies a range of process in the form of three integers for the first rank, last rank, and stride.

  - *newgroup* \[out\]  
    A pointer to a handle that represents the new group. The new group contains the additional sets of ranks. The order is defined by *ranges*.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_RANGE_INCL(GROUP, N, RANGES, NEWGROUP, IERROR)
        INTEGER GROUP, N, RANGES(3,*), NEWGROUP, IERROR
```

## Remarks

If ranges consist of the triplets (first1 , last1, stride1) , ..., (firstn, lastn, striden), then *newgroup* consists of the sequence of processes in *group* with ranks first1, first1 + stride1, ..., **RoundDown**((last1 - first1)/stride1)\*stride1, ..., firstn, firstn + striden, ..., **RoundDown**((lastn - firstn)/striden)\*striden.

Each computed rank must be a valid rank in the new group, and all computed ranks must be distinct. Otherwise, the function returns an error.

> [!NOTE]
> Note that you can set *first\[i\]* greater than *last\[i\]*, and *stride\[i\]* can be negative, but it cannot be zero.

 

This is a local operation. Different processes can define distinct groups. A process can define a group that does not include itself.

The MPI implementation does not provide a mechanism to build a group from scratch, but only from existing groups. The base group, upon which all other groups are defined, can be retrieved by using the [**MPI\_Comm\_group**](mpi-comm-group-function.md) function. It is the group that is associated with the initial communicator **MPI\_COMM\_WORLD**.

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

[MPI Group Functions](mpi-group-functions.md)

[**MPI\_Group\_incl**](mpi-group-incl-function.md)

[**MPI\_Comm\_group**](mpi-comm-group-function.md)

