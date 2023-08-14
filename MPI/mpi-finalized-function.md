---
title: MPI_Finalized function
TOCTitle: MPI_Finalized function
ms:assetid: d7fc4031-59e9-47a6-9e84-be306cbc5c8a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473373(v=VS.85)
ms:contentKeyID: 59360909
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FINALIZED
- mpif/MPI_Finalized
- mpi/MPI_FINALIZED
dev_langs:
- C++
- C
description: Learn Microsoft MPI_Finalized Function: Discover syntax, parameters, and return values for Message Passing Interface. Maximize HPC efficiency.
---

# MPI\_Finalized function

Indicates whether [**MPI\_Finalize**](mpi-finalize-function.md) has been called.

## Syntax

``` c++
int MPIAPI MPI_Finalized(
  _Out_ int *flag
);
```

## Parameters

  - *flag* \[out\]  
    Flag is true if [**MPI\_Finalize**](mpi-finalize-function.md) has been called and false otherwise.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FINALIZED(FLAG, IERROR)
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

