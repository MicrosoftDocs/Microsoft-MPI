---
title: MPI_Grequest_free_function callback function
TOCTitle: MPI_Grequest_free_function callback function
ms:assetid: b1a96d01-0a0c-4307-9cf2-68b51426e45e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473392(v=VS.85)
ms:contentKeyID: 59360928
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- GREQUEST_FREE_FUNCTION
- mpi/GREQUEST_FREE_FUNCTION
- mpi/MPI_Grequest_free_function
- MPI_Grequest_free_function
- mpif/GREQUEST_FREE_FUNCTION
- mpif/MPI_Grequest_free_function
dev_langs:
- C++
- C
---

# MPI\_Grequest\_free\_function callback function

**MPI\_Grequest\_free\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Grequest_free_function(
  _In_opt_ void *extra_state
);
```

## Parameters

  - *extra\_state* \[in, optional\]  
    TBD

## Return value

TBD

## Fortran

    SUBROUTINE GREQUEST_FREE_FUNCTION(EXTRA_STATE, IERROR)
        INTEGER IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE

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
</tbody>
</table>


## See also

[MPI External Functions](mpi-external-functions.md)

[**MPI\_Grequest\_start**](mpi-grequest-start-function.md)

