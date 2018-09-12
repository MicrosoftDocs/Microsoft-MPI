---
title: MPI_Type_create_indexed_block function
TOCTitle: MPI_Type_create_indexed_block function
ms:assetid: c093ef03-d22e-43cb-b5aa-641d53705fc9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473493(v=VS.85)
ms:contentKeyID: 59361028
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_INDEXED_BLOCK
- mpif/MPI_Type_create_indexed_block
- mpi/MPI_TYPE_CREATE_INDEXED_BLOCK
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_indexed_block
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

# MPI\_Type\_create\_indexed\_block function

Defines a new data type that consists of a specified number of blocks. Each block is the same block length, but each block can have a different block displacement.

## Syntax

``` c++
int MPIAPI MPI_Type_create_indexed_block(
        int                   count,
        int                   blocklength,
        _In_count_(count) int array_of_displacements[],
        MPI_Datatype          oldtype,
  _Out_ MPI_Datatype          *newtype
);
```

## Parameters

  - *count*  
    The number of blocks and the number of entries in the *array\_of\_displacements* parameter.

  - *blocklength*  
    The number of elements in each block.

  - *array\_of\_displacements*  
    The displacement of each individual block in bytes. All block displacements must be a multiple of the **extent** of the data type as specified in the *oldtype* parameter.

  - *oldtype*  
    The MPI data type of each element.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_INDEXED_BLOCK(COUNT, BLOCKLENGTH, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR)
        COUNT, BLOCKLENGTH, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR
```

## Remarks

This function is similar to the function [**MPI\_Type\_indexed**](mpi-type-indexed-function.md) except that all the blocks have the same length.

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

[MPI Datatype Functions](mpi-datatype-functions.md)

[**MPI\_Type\_indexed**](mpi-type-indexed-function.md)

