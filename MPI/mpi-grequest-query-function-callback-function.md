---
title: MPI_Grequest_query_function callback function
TOCTitle: MPI_Grequest_query_function callback function
ms:assetid: 5b15fa89-832a-428d-87b7-efd393a20ea1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473393(v=VS.85)
ms:contentKeyID: 59360929
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- GREQUEST_QUERY_FUNCTION
- mpi/GREQUEST_QUERY_FUNCTION
- mpi/MPI_Grequest_query_function
- MPI_Grequest_query_function
- mpif/GREQUEST_QUERY_FUNCTION
- mpif/MPI_Grequest_query_function
dev_langs:
- C++
- C
---

# MPI\_Grequest\_query\_function callback function

**MPI\_Grequest\_query\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Grequest_query_function(
  _In_opt_ void       *extra_state,
  _Out_    MPI_Status *status
);
```

## Parameters

  - *extra\_state* \[in, optional\]  
    TBD

  - *status* \[out\]  
    TBD

## Return value

TBD

## Fortran

    SUBROUTINE GREQUEST_QUERY_FUNCTION(EXTRA_STATE, STATUS, IERROR)
        INTEGER STATUS(MPI_STATUS_SIZE), IERROR
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

