---
title: MPI_Type_create_hvector function
TOCTitle: MPI_Type_create_hvector function
ms:assetid: 66f3fd82-d20c-4ac0-a5e1-ab54115df59f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473492(v=VS.85)
ms:contentKeyID: 59361027
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_HVECTOR
- mpif/MPI_Type_create_hvector
- mpi/MPI_TYPE_CREATE_HVECTOR
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_create_hvector
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about MPI_Type_create_hvector function, a new data type defining method with specified blocks and elements. Understand its syntax, parameters, and usage.
---

# MPI\_Type\_create\_hvector function

Defines a new data type that consists of a specified number of blocks. Each block is a concatenation of the same number of elements of an existing data type. This function is similar to the function [**MPI\_Type\_vector**](mpi-type-vector-function.md) except that the stride is specified in bytes instead of the number of elements.

## Syntax

``` c++
int MPIAPI MPI_Type_create_hvector(
        int          count,
        int          blocklength,
        MPI_Aint     stride,
        MPI_Datatype oldtype,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *count*  
    The number of blocks in the new data type.

  - *blocklength*  
    The number of elements in each block.

  - *stride*  
    The number of bytes between the start of one block and the next. The stride is a multiple of the **extent** of the old data type.

  - *oldtype*  
    The MPI data type of each element.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_HVECTOR(COUNT, BLOCKLENGTH, STRIDE, OLDTYPE, NEWTYPE, IERROR)
        INTEGER COUNT, BLOCKLENGTH, STRIDE, OLDTYPE, NEWTYPE, IERROR
```

## Remarks

This function replaces the **MPI\_Type\_hvector** function, which is deprecated.

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

[**MPI\_Type\_contiguous**](mpi-type-contiguous-function.md)

[**MPI\_Type\_vector**](mpi-type-vector-function.md)

