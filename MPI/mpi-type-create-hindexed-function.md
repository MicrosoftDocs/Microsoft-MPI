---
title: MPI_Type_create_hindexed function
TOCTitle: MPI_Type_create_hindexed function
ms:assetid: 07b5a612-29be-46f9-b91e-1cbc387baf78
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473491(v=VS.85)
ms:contentKeyID: 59361026
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_HINDEXED
- mpif/MPI_Type_create_hindexed
- mpi/MPI_TYPE_CREATE_HINDEXED
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_hindexed
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Type_create_hindexed function with this comprehensive guide. Learn about its syntax, parameters, and usage in data block creation.
---

# MPI\_Type\_create\_hindexed function

Defines a new data type that consists of a specified number of blocks of arbitrary size. Each block is a concatenation of elements of an existing data type. Each block can contain a different number of elements and have a different displacement.

## Syntax

``` c++
int MPIAPI MPI_Type_create_hindexed(
        int                        count,
        _In_count_(count) int      array_of_blocklengths[],
        _In_count_(count) MPI_Aint array_of_displacements[],
        MPI_Datatype               oldtype,
  _Out_ MPI_Datatype               *newtype
);
```

## Parameters

  - *count*  
    The number of blocks and the number of entries in the *array\_of\_blocklengths* and *array\_of\_displacements* parameters.

  - *array\_of\_blocklengths*  
    The number of elements of each block.

  - *array\_of\_displacements*  
    The displacement of each block in bytes.

  - *oldtype*  
    The MPI data type of each element.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_HINDEXED(COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR)
        COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR
```

## Remarks

This function replaces the **MPI\_Type\_hindexed**, which is deprecated.

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

[MPI Datatype Functions](mpi-datatype-functions.md)

[**MPI\_Type\_indexed**](mpi-type-indexed-function.md)

