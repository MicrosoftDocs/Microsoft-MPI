---
title: MPI_Type_create_f90_integer function
TOCTitle: MPI_Type_create_f90_integer function
ms:assetid: 150faece-b5d8-4359-9efb-07ca41d75997
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473489(v=VS.85)
ms:contentKeyID: 59361024
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_F90_INTEGER
- mpif/MPI_Type_create_f90_integer
- mpi/MPI_TYPE_CREATE_F90_INTEGER
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_f90\_integer function

Returns a predefined type that matches the specified range.

## Syntax

``` c++
int MPIAPI MPI_Type_create_f90_integer(
        int          r,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *r*  
    Decimal range (number of digits) desired.

  - *newtype* \[out\]  
    A predefine MPI Datatype that matches the range.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_CREATE_F90_INTEGER(R, NEWTYPE, IERROR)
        INTEGER R, NEWTYPE, IERROR

## Remarks

This function returns a predefined MPI datatype that matches a INTEGER variable of *KIND selected_int_kind\(r\)*. Matching rules for datatypes created by this function are analogous to the matching rules for datatypes created by [**MPI\_Type\_create\_f90\_real**](mpi-type-create-f90-real-function.md).

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

