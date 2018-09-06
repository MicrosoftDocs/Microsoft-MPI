---
title: MPI_Type_create_darray function
TOCTitle: MPI_Type_create_darray function
ms:assetid: 59ada82e-1178-4059-bc07-3f0426a62297
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473487(v=VS.85)
ms:contentKeyID: 59361022
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_DARRAY
- mpif/MPI_Type_create_darray
- mpi/MPI_TYPE_CREATE_DARRAY
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_darray function

Creates a datatype representing a distributed array.

## Syntax

``` c++
int MPIAPI MPI_Type_create_darray(
        int                   size,
        int                   rank,
        int                   ndims,
        _In_count_(ndims) int array_of_gszies[],
        _In_count_(ndims) int array_of_distribs[],
        _In_count_(ndims) int array_of_dargs[],
        _In_count_(ndims) int array_of_psizes[],
        int                   order,
        MPI_Datatype          oldtype,
  _Out_ MPI_Datatype          *newtype
);
```

## Parameters

  - *size*  
    Size of process group.

  - *rank*  
    Rank in process group.

  - *ndims*  
    Number of array dimensions as well as process grid dimensions.

  - *array\_of\_gszies*  
    Number of elements of type *oldtype* in each dimension of global array.

  - *array\_of\_distribs*  
    Distribution of array in each dimension.

  - *array\_of\_dargs*  
    Distribution argument in each dimension.

  - *array\_of\_psizes*  
    Size of process grid in each dimension.

  - *order*  
    Array storage order flag.

  - *oldtype*  
    Old datatype.

  - *newtype* \[out\]  
    New datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_CREATE_DARRAY(SIZE, RANK, NDIMS, ARRAY_OF_GSIZES,
            ARRAY_OF_DISTRIBS, ARRAY_OF_DARGS, ARRAY_OF_PSIZES, ORDER,
            OLDTYPE, NEWTYPE, IERROR)
        INTEGER SIZE, RANK, NDIMS, ARRAY_OF_GSIZES(*), ARRAY_OF_DISTRIBS(*),
        ARRAY_OF_DARGS(*), ARRAY_OF_PSIZES(*), ORDER, OLDTYPE, NEWTYPE, IERROR

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

