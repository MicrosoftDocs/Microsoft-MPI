---
title: MPI_Type_create_resized function
TOCTitle: MPI_Type_create_resized function
ms:assetid: 42b179ed-d5a9-4819-ac6b-88ebf868a90f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520559(v=VS.85)
ms:contentKeyID: 59361030
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_RESIZED
- mpif/MPI_Type_create_resized
- mpi/MPI_TYPE_CREATE_RESIZED
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_resized function

Creates a datatype with a new lower bound and extent from an existing datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_create_resized(
        MPI_Datatype oldtype,
        MPI_Aint     lb,
        MPI_Aint     extent,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *oldtype*  
    Input datatype.

  - *lb*  
    New lower bound of datatype.

  - *extent*  
    New extent of datatype.

  - *newtype* \[out\]  
    Output datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_RESIZED(OLDTYPE, LB, EXTENT, NEWTYPE, IERROR)
        INTEGER OLDTYPE, NEWTYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) LB, EXTENT
```

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

