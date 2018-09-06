---
title: MPI_Testany function
TOCTitle: MPI_Testany function
ms:assetid: 9C4B9B43-3569-4252-8284-5DBE1229915D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473481(v=VS.85)
ms:contentKeyID: 59361016
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TESTANY
- mpif/MPI_Testany
- mpi/MPI_TESTANY
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Testany
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Testany function

Tests for completion of any previdously initiated requests.

## Syntax

``` c++
int MPIAPI MPI_Testany(
        int                              count,
        _Inout_count_(count) MPI_Request *array_of_requests,
  _Out_ int                              *index,
  _Out_ MPI_Status                       *status
);
```

## Parameters

  - *count*  
    The number of entries in *array\_of\_requests* parameter.

  - *array\_of\_requests*  
    An array of **MPI\_Request** handles of outstanding operations.

  - *index* \[out\]  
    A pointer to an integer indicating the index in the *array\_of\_requests* parameter of the operation that completed. The array is indexed from zero in C, and from one in Fortran.

  - *status* \[out\]  
    A pointer to an [**MPI\_Status**](mpi-status-structure.md) object describing the completed operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TESTANY(COUNT, ARRAY_OF_REQUESTS, INDEX, FLAG, STATUS, IERROR) LOGICAL FLAG
        INTEGER COUNT, ARRAY_OF_REQUESTS(*), INDEX, STATUS(MPI_STATUS_SIZE), IERROR

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

