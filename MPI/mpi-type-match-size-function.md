---
title: MPI_Type_match_size function
TOCTitle: MPI_Type_match_size function
ms:assetid: 2c06213e-42da-4e6f-b8b0-2ac39fcbe3b8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520578(v=VS.85)
ms:contentKeyID: 59361049
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_MATCH_SIZE
- mpif/MPI_Type_match_size
- mpi/MPI_TYPE_MATCH_SIZE
dev_langs:
- C++
- C
---

# MPI\_Type\_match\_size function

Finds an MPI datatype matching a specified size.

## Syntax

``` c++
int MPIAPI MPI_Type_match_size(
        int          typeclass,
        int          size,
  _Out_ MPI_Datatype *type
);
```

## Parameters

  - *typeclass*  
    Generic type specifier.

  - *size*  
    Size of representation in bytes.

  - *type* \[out\]  
    Datatype with correct type, size.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_MATCH_SIZE(TYPECLASS, SIZE, DATATYPE, IERROR)
        INTEGER TYPECLASS, SIZE, DATATYPE, IERROR

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilitiese</p></td>
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

