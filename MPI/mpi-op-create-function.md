---
title: MPI_Op_create function
TOCTitle: MPI_Op_create function
ms:assetid: 5b636d07-7c9c-4164-8a08-d3a9e37cfe41
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473438(v=VS.85)
ms:contentKeyID: 59360974
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_OP_CREATE
- MPI_OP_CREATE
- mpif/MPI_Op_create
dev_langs:
- C++
- C
---

# MPI\_Op\_create function

Creates a user-defined combination function handle.

## Syntax

``` c++
int MPIAPI MPI_Op_create(
  _In_  MPI_User_function *function,
        int               commute,
  _Out_ MPI_Op            *op
);
```

## Parameters

  - *function* \[in\]  
    User defined function.

  - *commute*  
    True if commutative, false otherwise.

  - *op* \[out\]  
    Operation object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_OP_CREATE( USER_FN, COMMUTE, OP, IERROR)
        EXTERNAL USER_FN
        LOGICAL COMMUTE
        INTEGER OP, IERROR

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
<td>Mpif.h;
Mpi.h</td>
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

[MPI Collective Functions](mpi-collective-functions.md)

[**MPI\_User\_function**](mpi-user-function-function.md)

