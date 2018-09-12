---
title: MPI_Initialized function
TOCTitle: MPI_Initialized function
ms:assetid: fae67e86-8a12-4dc0-9c65-ec1aa63c7eb4
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473420(v=VS.85)
ms:contentKeyID: 59360956
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INITIALIZED
- mpif/MPI_Initialized
- mpi/MPI_INITIALIZED
dev_langs:
- C++
- C
---

# MPI\_Initialized function

Indicates whether [**MPI\_Init**](mpi-init-function.md) has been called.

## Syntax

``` c++
int MPIAPI MPI_Initialized(
  _Out_ int *flag
);
```

## Parameters

  - *flag* \[out\]  
    Flag is true if [**MPI\_Init**](mpi-init-function.md) or [**MPI\_Init\_thread**](mpi-init-thread-function.md) has been called and false otherwise.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INITIALIZED(FLAG, IERROR)
        LOGICAL FLAG
        INTEGER IERROR
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

[MPI Management Functions](mpi-management-functions.md)

