---
title: MPI_Datarep_extent_function callback function
TOCTitle: MPI_Datarep_extent_function callback function
ms:assetid: 0a58ab96-146a-42af-871c-0acbd21df042
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473289(v=VS.85)
ms:contentKeyID: 59360835
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- DATAREP_EXTENT_FUNCTION
- mpi/DATAREP_EXTENT_FUNCTION
- mpi/MPI_Datarep_extent_function
- MPI_Datarep_extent_function
- mpif/DATAREP_EXTENT_FUNCTION
- mpif/MPI_Datarep_extent_function
dev_langs:
- C++
- C
description: Explore the MPI_Datarep_extent_function callback function on Microsoft's learning platform. Understand its syntax, parameters, and usage in user-defined extent functions.
---

# MPI\_Datarep\_extent\_function callback function

This function is a placeholder for user-defined extent callback functions.

## Syntax

``` c++
int MPI_Datarep_extent_function(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *file_extent,
  _In_  void         *extra_state
);
```

## Parameters

  - *datatype*  
    Datatype.

  - *file\_extent* \[out\]  
    The number of bytes required to store *datatype* in the file representation.

  - *extra\_state* \[in\]  
    The same argument that was passed to the [**MPI\_Register\_datarep**](mpi-register-datarep-function.md) call.

## Return value

The extent callback functions return an error code.

## Fortran

``` FORTRAN
    SUBROUTINE DATAREP_EXTENT_FUNCTION(DATATYPE, EXTENT, EXTRA_STATE, IERROR)
        INTEGER DATATYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTENT, EXTRA_STATE
```

## Remarks

MPI will only call this routine with predefined datatypes employed by the user.

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
</tbody>
</table>


## See also

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

[**MPI\_Register\_datarep**](mpi-register-datarep-function.md)

