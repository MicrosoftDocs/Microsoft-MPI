---
title: MPI_Waitsome function
TOCTitle: MPI_Waitsome function
ms:assetid: aa5b1b9f-7e49-4074-adb2-3e06b889baea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520592(v=VS.85)
ms:contentKeyID: 59361063
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WAITSOME
- mpif/MPI_Waitsome
- mpi/MPI_WAITSOME
dev_langs:
- C++
- C
description: Master the MPI_Waitsome function with this comprehensive guide. Learn syntax, parameters, return values, and more for successful message-passing operations.
---

# MPI\_Waitsome function

Completes some out of several outstanding operations.

## Syntax

``` c++
int MPIAPI MPI_Waitsome(
        int                                         incount,
        _Inout_count_(incount) MPI_Request          array_of_requests,
  _Out_ int                                         *outcount,
        _Out_cap_post_count_(incount,*outcount) int *array_of_indices,
        _Out_cap_post_count_(incount,*outcount)     *array_of_statuses
);
```

## Parameters

  - *incount*  
    The number of entries in the *array\_of\_requests* parameter.

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
    MPI_WAITSOME(INCOUNT, ARRAY_OF_REQUESTS, OUTCOUNT, ARRAY_OF_INDICES, ARRAY_OF_STATUSES, IERROR)
        INTEGER INCOUNT, ARRAY_OF_REQUESTS(*), OUTCOUNT, ARRAY_OF_INDICES(*),
        ARRAY_OF_STATUSES(MPI_STATUS_SIZE,*), IERROR
```

## Remarks

The array of indicies are in the range *0* to *incount - 1* for C and in the range *1* to *incount* for Fortran.

**NULL** requests are ignored; if all requests are **NULL**, then the routine returns with *outcount* set to **MPI\_UNDEFINED**.

While it is possible to list a request handle more than once in the *array\_of\_requests*, such an action is considered erroneous and may cause the program to unexecpectedly terminate or produce incorrect results.

[**MPI\_Waitsome**](mpi-waitsome-function.md) provides an interface much like the Unix 'select' or 'poll' calls and, in a high qualilty implementation, indicates all of the requests that have completed when [**MPI\_Waitsome**](mpi-waitsome-function.md) is called. However, [**MPI\_Waitsome**](mpi-waitsome-function.md) only guarantees that at least one request has completed; there is no guarantee that **all** completed requests will be returned, or that the entries in *array\_of\_indices* will be in increasing order. Also, requests that are completed while [**MPI\_Waitsome**](mpi-waitsome-function.md) is executing may or may not be returned, depending on the timing of the completion of the message.


## Requirements

<table>
<colgroup>
<col  />
<col  />
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

