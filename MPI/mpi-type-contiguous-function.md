---
title: MPI_Type_contiguous function
TOCTitle: MPI_Type_contiguous function
ms:assetid: f2fb753c-3f17-4308-a384-8edd8c18bacf
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473485(v=VS.85)
ms:contentKeyID: 59361020
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CONTIGUOUS
- mpif/MPI_Type_contiguous
- mpi/MPI_TYPE_CONTIGUOUS
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Type_contiguous
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

# MPI\_Type\_contiguous function

Defines a new data type that is a concatenation of a number of elements of an existing data type.

## Syntax

``` c++
int MPIAPI MPI_Type_contiguous(
        int          count,
        MPI_Datatype oldtype,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *count*  
    The number of elements in the new data type.

  - *oldtype*  
    The MPI data type of each element.

  - *newtype* \[out\]  
    On return, contains an [**MPI\_Datatype**](mpi-datatype-enumeration.md) handle that represents the new data type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_CONTIGUOUS(COUNT, OLDTYPE, NEWTYPE, IERROR)
        INTEGER COUNT, OLDTYPE, NEWTYPE, IERROR

## Remarks

The concatenation of the new data type is defined by using the extent of the old data type as the size of the concatenated copies.

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

[**MPI\_Type\_vector**](mpi-type-vector-function.md)

[**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md)

