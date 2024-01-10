---
title: MPI_Type_vector function
TOCTitle: MPI_Type_vector function
ms:assetid: 1bb8716f-8dc1-4b3a-8f2b-5177c63db715
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520584(v=VS.85)
ms:contentKeyID: 59361055
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_VECTOR
- mpif/MPI_Type_vector
- mpi/MPI_TYPE_VECTOR
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_vector
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to define a new data type with MPI_Type_vector function on Microsoft's platform. Understand syntax, parameters, and return values.
---

# MPI\_Type\_vector function

Defines a new data type that consists of a specified number of blocks of a specified size. Each block is a concatenation of the same number of elements of an existing data type.

## Syntax

``` c++
int MPIAPI MPI_Type_vector(
        int          count,
        int          blocklength,
        int          stride,
        MPI_Datatype oldtype,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *count*  
    The number of blocks in the created vector.

  - *blocklength*  
    The number of elements in each block.

  - *stride*  
    The number of elements between the start of one block and the start of the next block.

  - *oldtype*  
    The data type of each element.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_VECTOR(COUNT, BLOCKLENGTH, STRIDE, OLDTYPE, NEWTYPE, IERROR)
        INTEGER COUNT, BLOCKLENGTH, STRIDE, OLDTYPE, NEWTYPE, IERROR
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

[MPI Datatype Functions](mpi-datatype-functions.md)

[**MPI\_Type\_contiguous**](mpi-type-contiguous-function.md)

[**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md)

