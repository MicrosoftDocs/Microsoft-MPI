---
title: MPI_Type_create_subarray function
TOCTitle: MPI_Type_create_subarray function
ms:assetid: 27B8E756-94C6-43A9-ACDD-A583419C40A5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520561(v=VS.85)
ms:contentKeyID: 59361032
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_TYPE_CREATE_SUBARRAY
- MPI_ORDER_C
- MPI_ORDER_FORTRAN
- MPI_TYPE_CREATE_SUBARRAY
- mpif/MPI_Type_create_subarray
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_subarray
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about MPI_Type_create_subarray function, a new data type for n-dimensional subarrays. Understand syntax, parameters, and error handling.
---

# MPI\_Type\_create\_subarray function

Defines a new data type that consists of an n-dimensional subarray of an n-dimensional array. The subarray can be located anywhere within the full array. It can be any nonzero size as long as it is fully contained within the array.

## Syntax

``` c++
int MPIAPI MPI_Type_create_subarray(
        int                   ndims,
        _In_count_(ndims) int array_of_sizes[],
        _In_count_(ndims) int array_of_subsizes[],
        _In_count_(ndims) int array_of_starts[],
        int                   order,
        MPI_Datatype          oldtype,
  _Out_ MPI_Datatype          *newtype
);
```

## Parameters

*ndims*

The number of array dimensions and the number of elements in the *array\_of\_sizes*, *array\_of\_subsizes* and *array\_of\_starts* parameters.

*array\_of\_sizes*

The number of elements in each dimension of the full array.

*array\_of\_subsizes*

The number of elements in each dimension of the subarray.

*array\_of\_starts*

The starting index of the subarray in each dimension.

*order*

The order of the dimensions.

**MPI\_ORDER\_C**

The row-major order in which all the elements for a given row are stored contiguously.

**MPI\_ORDER\_FORTRAN**

The column-major order in which all the elements for a given column are stored contiguously.

> [!NOTE]
> Both C and Fortran programs can use either order. The defined values reflect typical usage.

 

*oldtype*

Specifies the data type of each element.

*newtype* \[out\]

On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_SUBARRAY(NDIMS, ARRAY_OF_SIZES, ARRAY_OF_SUBSIZES, ARRAY_OF_STARTS, ORDER, OLDTYPE, NEWTYPE, IERROR)
        NDIMS, ARRAY_OF_SIZES, ARRAY_OF_SUBSIZES, ARRAY_OF_STARTS, ORDER, OLDTYPE, NEWTYPE, IERROR
```

## Remarks

The function returns an error if the size of the subarray exceeds the size of the array. For each dimension *i*, the value of *array\_of\_subsizes\[i\]* parameter must be greater than or equal to one and less than or equal to the *array\_of\_sizes\[i\]* parameter.

The function returns an error if the subarray starts or ends outside the bounds of the array. For any dimension *i*, the value of parameter must be zero and the sum of the *array\_of\_starts\[i\]* and *array\_of\_subsizes\[i\]* parameters must be less than or equal to the value of the *array\_of\_sizes\[i\]* parameter. For example, if the subarray is the same size as the array, then the subarray must start at index zero. Arrays are assumed to be indexed starting from zero.

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

