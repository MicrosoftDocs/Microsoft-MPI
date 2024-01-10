---
title: MPI_Type_size function
TOCTitle: MPI_Type_size function
ms:assetid: f4ed33ce-5966-42b9-bc1c-d066d9b7dcec
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520581(v=VS.85)
ms:contentKeyID: 59361052
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_SIZE
- mpif/MPI_Type_size
- mpi/MPI_TYPE_SIZE
dev_langs:
- C++
- C
description: Learn about the MPI_Type_size function on Microsoft's site. Understand its syntax, parameters, return values, and its role in data type functions.
---

# MPI\_Type\_size function

Returns the number of bytes occupied by entries in the datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_size(
        MPI_Datatype datatype,
  _Out_ int          *size
);
```

## Parameters

  - *datatype*  
    Datatype.

  - *size* \[out\]  
    Size of the *datatype*.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_SIZE(DATATYPE, SIZE, IERROR)
        INTEGER DATATYPE, SIZE, IERROR
```

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

