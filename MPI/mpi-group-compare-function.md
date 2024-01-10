---
title: MPI_Group_compare function
TOCTitle: MPI_Group_compare function
ms:assetid: 2549da8a-673e-4ac3-8985-e5b49796582c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473395(v=VS.85)
ms:contentKeyID: 59360931
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IDENT
- MPI_SIMILAR
- MPI_UNEQUAL
- mpi/MPI_GROUP_COMPARE
- mpif/MPI_Group_compare
- MPI_GROUP_COMPARE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_compare
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Group_compare function on Microsoft's site. Understand its syntax, parameters, return values, and how it compares two groups for member equality.
---

# MPI\_Group\_compare function

Compares two groups for member equality.

## Syntax

``` c++
int MPIAPI MPI_Group_compare(
        MPI_Group group1,
        MPI_Group group2,
  _Out_ int       *result
);
```

## Parameters

*group1*

The first group.

*group2*

The second group.

*result* \[out\]

On return, points to an integer that indicates the results of the comparison.

**MPI\_IDENT**

Indicates that the group members and group order is exactly the same in both groups. For example, the function returns this value if group1 and group2 are the same handle.

**MPI\_SIMILAR**

Indicates that the group members are the same but the order is different.

**MPI\_UNEQUAL**

Indicates that the handles are for different objects.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_COMPARE(GROUP1, GROUP2, RESULT, IERROR)
        INTEGER GROUP1, GROUP2, RESULT, IERROR
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

