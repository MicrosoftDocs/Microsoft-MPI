---
title: MPI_Grequest_cancel_function callback function
TOCTitle: MPI_Grequest_cancel_function callback function
ms:assetid: 185973fe-26d2-4271-a581-df43908eb227
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473390(v=VS.85)
ms:contentKeyID: 59360926
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- GREQUEST_CANCEL_FUNCTION
- mpi/GREQUEST_CANCEL_FUNCTION
- mpi/MPI_Grequest_cancel_function
- MPI_Grequest_cancel_function
- mpif/GREQUEST_CANCEL_FUNCTION
- mpif/MPI_Grequest_cancel_function
dev_langs:
- C++
- C
---

# MPI\_Grequest\_cancel\_function callback function

**MPI\_Grequest\_cancel\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Grequest_cancel_function(
  _In_opt_ void *extra_state,
           int  complete
);
```

## Parameters

  - *extra\_state* \[in, optional\]  
    TBD

  - *complete*  
    TBD

## Return value

TBD

## Fortran

    SUBROUTINE GREQUEST_CANCEL_FUNCTION(EXTRA_STATE, COMPLETE, IERROR)
        INTEGER IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
        LOGICAL COMPLETE

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

