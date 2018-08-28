---
title: MPI_Comm_compare function
TOCTitle: MPI_Comm_compare function
ms:assetid: 881e2ef6-ad94-413b-82e0-89fe27534419
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473258(v=VS.85)
ms:contentKeyID: 59360804
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_COMM_COMPARE
- MPI_CONGRUENT
- MPI_IDENT
- MPI_SIMILAR
- MPI_UNEQUAL
- mpif/MPI_Comm_compare
- MPI_COMM_COMPARE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_compare
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

# MPI\_Comm\_compare function

Compares two communicator handles.

## Syntax

``` c++
int MPIAPI MPI_Comm_compare(
        MPI_Comm comm1,
        MPI_Comm comm2,
  _Out_ int      *result
);
```

## Parameters

*comm1*

A handle for the first communicator to compare.

*comm2*

A handle for the second communicator to compare.

*result* \[out\]

On return, a pointer to the results of the comparison.

The possible values are.

**MPI\_IDENT**

Indicates that the two handles are for the same object. The handles reference identical groups and contexts.

**MPI\_CONGRUENT**

Indicates that the underlying groups have identical members in the same rank order. These communicators differ only by context.

**MPI\_SIMILAR**

Indicates that the underlying groups have identical members, but they are in different rank orders.

**MPI\_UNEQUAL**

Indicates that the handles are for different objects.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_COMM_COMPARE(COMM1,COMM2,RESULT,IERROR)
        INTEGER COMM1, COMM1, RESULT, IERROR

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

