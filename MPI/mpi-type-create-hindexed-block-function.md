---
title: MPI_Type_create_hindexed_block function
TOCTitle: MPI_Type_create_hindexed_block function
ms:assetid: ED5D334D-FE5E-4259-A679-82B38C750873
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985834(v=VS.85)
ms:contentKeyID: 65288038
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_HINDEXED_BLOCK
- mpif/MPI_Type_create_hindexed_block
- mpi/MPI_TYPE_CREATE_HINDEXED_BLOCK
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_hindexed_block
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

# MPI\_Type\_create\_hindexed\_block function

Allows replication of an old datatype into a sequence of blocks (each block is a concatenation of the old datatype), where all blocks have the same block length but can have different block displacements in bytes.

## Syntax

``` c++
int MPIAPI MPI_Type_create_hindexed_block(
  _In_  int          count,
  _In_  int          blocklength,
  _In_  MPI_Aint     array_of_displacements[],
  _In_  MPI_Datatype oldtype,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *count* \[in\]  
    The number of blocks and the number of entries in the *array\_of\_displacements* parameter.

  - *blocklength* \[in\]  
    The number of elements in each block.

  - *array\_of\_displacements* \[in\]  
    The array containing the displacement of each block, in bytes.

  - *oldtype* \[in\]  
    The [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle representing the data type of each element.

  - *newtype* \[out\]  
    On return, contains the [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle representing a data type containing *count* copies of element blocks. Each block has *blocklength* elements. The displacement of each block is specified in *array\_of\_displacements*.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_HINDEXED_BLOCK(COUNT, BLOCKLENGTH, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR)
        INTEGER COUNT, BLOCKLENGTH, OLDTYPE, NEWTYPE, IERROR
    INTEGER(KIND=MPI_ADDRESS_KIND) ARRAY_OF_DISPLACEMENTS(*)
```

## Remarks

This function is similar to the function [**MPI\_Type\_create\_indexed\_block**](mpi-type-create-indexed-block-function.md) except that the array of displacements contains the displacement of each block in bytes.

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[**MPI\_Type\_create\_indexed\_block**](mpi-type-create-indexed-block-function.md)

