---
title: MPI_Test_cancelled function
TOCTitle: MPI_Test_cancelled function
ms:assetid: 4649c1b5-9202-4a0c-b48a-1faf55ce74ef
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473483(v=VS.85)
ms:contentKeyID: 59361018
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TEST_CANCELLED
- mpif/MPI_Test_cancelled
- mpi/MPI_TEST_CANCELLED
dev_langs:
- C++
- C
---

# MPI\_Test\_cancelled function

Tests to see if a request was cancelled.

## Syntax

``` c++
int MPIAPI MPI_Test_cancelled(
  _In_  MPI_Status *status,
  _Out_ int        *flag
);
```

## Parameters

  - *status* \[in\]  
    Status object.

  - *flag* \[out\]  
    True if the request was cancelled, false otherwise.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TEST_CANCELLED(STATUS, FLAG, IERROR)
        LOGICAL FLAG
        INTEGER STATUS(MPI_STATUS_SIZE), IERROR

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

