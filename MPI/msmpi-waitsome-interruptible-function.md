---
title: MSMPI_Waitsome_interruptible function
TOCTitle: MSMPI_Waitsome_interruptible function
ms:assetid: 42CB465D-3923-45C2-BF91-9E4B9308BF59
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520627(v=VS.85)
ms:contentKeyID: 59361098
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Waitsome_interruptible
- MSMPI_Waitsome_interruptible
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MSMPI_Waitsome_interruptible
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

# MSMPI\_Waitsome\_interruptible function

Waits until at least one of the operations that is associated with active handles in the list has finished, or the call is interrupted by another thread that calls [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md).

## Syntax

``` c++
int MPIAPI MSMPI_Waitsome_interruptible(
        int                                         incount,
        _Inout_count_(incount) MPI_Request          array_of_requests[],
  _Out_ int                                         *outcount,
        _Out_cap_post_count_(incount,*outcount) int array_of_indices[],
        _Out_cap_post_count_(incount,*outcount) int array_of_statuses[]
);
```

## Parameters

  - *incount*  
    The number of requests in the array *array\_of\_requests*.

  - *array\_of\_requests*  
    Array of request handles of the operations on which to wait for completion. If a request handle was allocated by a nonblocking communication function, then it is deallocated, and the associated handle is set to **MPI\_REQUEST\_NULL**.

  - *outcount* \[out\]  
    The number of requests that is specified in the *array\_of\_requests* parameter that are completed and the number of elements in the *array\_of\_indices* and *array\_of\_statuses* arrays.
    
    If the *array\_of\_requests* contains no active handles, then the function returns immediately with the *outcount* parameter set to **MPI\_UNDEFINED**.
    
    If this function is interrupted before any requests are completed, then the call returns with the *outcount* parameter set to zero.

  - *array\_of\_indices*  
    Returns the indices within the *array\_of\_requests* parameter of the operations that are completed. Array indexes are zero-based in C and one-based in Fortran.

  - *array\_of\_statuses*  
    Returns the status of the operations that are completed. The elements of this array correspond to the elements of the *array\_of\_indices* array.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

If the function returns an error other than **MPI\_ERR\_IN\_STATUS**, it does not update the error fields of the statuses in the *array\_of\_statuses* parameter.

## Remarks

In a multi-threaded environment, users must obtain the global Microsoft MPI lock by using the [**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md) function before they call **MSMPI\_Waitsome\_interruptible**. This function is interrupted when another thread calls the **MSMPI\_Queuelock\_acquire** function in order to access the MPI library.

This function is an extension to the standard.

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
<td>Mpi.h</td>
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

[**MSMPI\_Lock\_queue**](msmpi-lock-queue-structure.md)

[**MSMPI\_Queuelock\_acquire**](msmpi-queuelock-acquire-function.md)

[**MSMPI\_Queuelock\_release**](msmpi-queuelock-release-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

