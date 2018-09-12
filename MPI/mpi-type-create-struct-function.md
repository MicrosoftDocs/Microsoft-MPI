---
title: MPI_Type_create_struct function
TOCTitle: MPI_Type_create_struct function
ms:assetid: a6c7a1fd-66e2-4dc0-a306-966b6c04cc86
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520560(v=VS.85)
ms:contentKeyID: 59361031
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_STRUCT
- mpif/MPI_Type_create_struct
- mpi/MPI_TYPE_CREATE_STRUCT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_struct
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

# MPI\_Type\_create\_struct function

Defines a new data type with a specified data type, displacement, and size for each block of data.

## Syntax

``` c++
int MPIAPI MPI_Type_create_struct(
        int                            count,
        _In_count_(count) int          array_of_blocklengths[],
        _In_count_(count) MPI_Aint     array_of_displacements[],
        _In_count_(count) MPI_Datatype array_of_types[],
  _Out_ MPI_Datatype                   *newtype
);
```

## Parameters

  - *count*  
    The number of blocks and the number of entries in the *array\_of\_blocklengths*, *array\_of\_displacements* and *array\_of\_types* parameters.

  - *array\_of\_blocklengths*  
    The number of elements of each block.

  - *array\_of\_displacements*  
    The displacement of each individual block in bytes.

  - *array\_of\_types*  
    The data type of each individual block.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_STRUCT(COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, ARRAY_OF_TYPES, NEWTYPE, IERROR)
        COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, ARRAY_OF_TYPES, NEWTYPE, IERROR
```

## Remarks

This function replaces the **MPI\_Type\_struct** function, which is deprecated.

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

[**MPI\_Type\_create\_hindexed**](mpi-type-create-hindexed-function.md)

[**MPI\_Type\_create\_indexed\_block**](mpi-type-create-indexed-block-function.md)

