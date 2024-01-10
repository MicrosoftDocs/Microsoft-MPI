---
title: MPI_Type_set_name function
TOCTitle: MPI_Type_set_name function
ms:assetid: af95499c-d3c7-4efe-a38f-da5c1a5ddc20
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520580(v=VS.85)
ms:contentKeyID: 59361051
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_SET_NAME
- mpif/MPI_Type_set_name
- mpi/MPI_TYPE_SET_NAME
dev_langs:
- C++
- C
---

# MPI\_Type\_set\_name function

Sets datatype name.

## Syntax

``` c++
int MPIAPI MPI_Type_set_name(
   MPI_Datatype type,
   _In_z_ char  *type_name
);
```

## Parameters

  - *type*  
    Datatype whose identifier is to be set.

  - *type\_name*  
    The character string which is set as the name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_SET_NAME(DATATYPE, TYPE_NAME, IERROR)
        INTEGER DATATYPE, IERROR
        CHARACTER*(*) TYPE_NAME
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

