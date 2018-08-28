---
title: MPI_Grequest_start function
TOCTitle: MPI_Grequest_start function
ms:assetid: e87295c3-6e39-4b47-aa6b-2398b6d3508a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473394(v=VS.85)
ms:contentKeyID: 59360930
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GREQUEST_START
- mpif/MPI_Grequest_start
- mpi/MPI_GREQUEST_START
dev_langs:
- C++
- C
---

# MPI\_Grequest\_start function

TBD

## Syntax

``` c++
int MPIAPI MPI_Grequest_start(
  _In_     MPI_Grequest_query_function  *query_fn,
  _In_     MPI_Grequest_free_function   *free_fn,
  _In_     MPI_Grequest_cancel_function *cancel_fn,
  _In_opt_ void                         *extra_state,
  _Out_    MPI_Request                  *request
);
```

## Parameters

  - *query\_fn* \[in\]  
    TBD

  - *free\_fn* \[in\]  
    TBD

  - *cancel\_fn* \[in\]  
    TBD

  - *extra\_state* \[in, optional\]  
    TBD

  - *request* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_GREQUEST_START(QUERY_FN, FREE_FN, CANCEL_FN, EXTRA_STATE, REQUEST, IERROR)
        INTEGER REQUEST, IERROR
        EXTERNAL QUERY_FN, FREE_FN, CANCEL_FN
        INTEGER (KIND=MPI_ADDRESS_KIND) EXTRA_STATE

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

[MPI External Functions](mpi-external-functions.md)

[*MPI\_Grequest\_query\_function*](mpi-grequest-query-function-callback-function.md)

[*MPI\_Grequest\_free\_function*](mpi-grequest-free-function-callback-function.md)

[*MPI\_Grequest\_cancel\_function*](mpi-grequest-cancel-function-callback-function.md)

