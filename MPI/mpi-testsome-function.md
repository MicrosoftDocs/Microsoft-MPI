---
title: MPI_Testsome function
TOCTitle: MPI_Testsome function
ms:assetid: 0cc7936e-e68b-4693-98a8-53d52b05d4b2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473482(v=VS.85)
ms:contentKeyID: 59361017
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TESTSOME
- mpif/MPI_Testsome
- mpi/MPI_TESTSOME
dev_langs:
- C++
- C
description: Learn about the MPI_Testsome function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements.
---

# MPI\_Testsome function

 Tests for some of given requests to complete.

## Syntax

``` c++
int MPIAPI MPI_Testsome(
        int                                                incount,
        _Inout_count_(incount) MPI_Request                 *array_of_requests,
  _Out_ int                                                *outcount,
        _Out_cap_post_count_(incount,*outcount) int        *array_of_indices,
        _Out_cap_post_count_(incount,*outcount) MPI_Status *array_of_statuses
);
```

## Parameters

  - *incount*  
    The number of entries in *array\_of\_requests* parameter.

  - *array\_of\_requests*  
    An array of **MPI\_Request** handles of outstanding operations.

  - *outcount* \[out\]  
    The number of completed requests.

  - *array\_of\_indices*  
    Array of indices in the *array\_of\_requests* of operations that completed. The *array\_of\_requests* is indexed from zero in C, and from one in Fortran.

  - *array\_of\_statuses*  
    Array of status objects for operations that completed, or **MPI\_STATUSES\_IGNORE**.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TESTSOME(INCOUNT, ARRAY_OF_REQUESTS, OUTCOUNT, ARRAY_OF_INDICES, ARRAY_OF_STATUSES, IERROR)
        INTEGER INCOUNT, ARRAY_OF_REQUESTS(*), OUTCOUNT, ARRAY_OF_INDICES(*),
        ARRAY_OF_STATUSES(MPI_STATUS_SIZE,*), IERROR
```

## Remarks

While it is possible to list a request handle more than once in the *array\_of\_requests*, such an action is considered erroneous and may cause the program to unexecpectedly terminate or produce incorrect results.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

