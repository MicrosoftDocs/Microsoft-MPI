---
title: MPI_Type_dup function
TOCTitle: MPI_Type_dup function
ms:assetid: 2e3f1d0b-5b14-4d14-b81d-c35a2793b7ea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520564(v=VS.85)
ms:contentKeyID: 59361035
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_DUP
- mpif/MPI_Type_dup
- mpi/MPI_TYPE_DUP
dev_langs:
- C++
- C
---

# MPI\_Type\_dup function

Duplicates a datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_dup(
        MPI_Datatype type,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *type*  
    Datatype to duplicate.

  - *newtype* \[out\]  
    Copy of type.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_DUP(OLDTYPE, NEWTYPE, IERROR)
        INTEGER OLDTYPE, NEWTYPE, IERROR

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

