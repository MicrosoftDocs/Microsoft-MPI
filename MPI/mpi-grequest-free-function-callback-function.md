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
    Extra state.

## Return value

All callback functions return an error code. The code is passed back and dealt with as appropriate for the error code by the MPI function that invoked the callback function. For example, if error codes are returned then the error code returned by the callback function will be returned by the MPI function that invoked the callback function. In the case of an [**MPI\_Waitany**](mpi-waitany-function.md) and [**MPI\_Testany**](mpi-testany-function.md) call that invokes both *query\_fn* and *free\_fn*, the MPI call will return the error code returned by the last callback, namely *free\_fn*. If one or more of the requests in a call to [**MPI\_Waitsome**](mpi-waitsome-function.md), [**MPI\_Waitall**](mpi-waitall-function.md), [**MPI\_Testsome**](mpi-testsome-function.md), or [**MPI\_Testall**](mpi-testall-function.md)  failed, then the MPI call will return **MPI\_ERR\_IN\_STATUS**. In such a case, if the MPI call was passed an array of statuses, then MPI will return in each of the statuses that correspond to a completed generalized request the error code returned by the corresponding invocation of its *free\_fn* callback function. However, if the MPI function was passed **MPI\_STATUSES\_IGNORE**, then the individual error codes returned by each callback functions will be lost.

## Fortran

    SUBROUTINE GREQUEST_FREE_FUNCTION(EXTRA_STATE, IERROR)
        INTEGER IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE

## Remarks

The *free\_fn* function is invoked to clean up user-allocated resources when the generalized request is freed. 

The *free\_fn* callback is invoked by the **MPI\_{Wait|Test}{any|some|all}** call that completed the generalized request associated with this callback. *free\_fn* is invoked after the call to *query\_fn* for the same request. However, if the MPI call completed multiple generalized requests, the order in which *free\_fn* callback functions are invoked is not specified by MPI.

The *free\_fn* callback is also invoked for generalized requests that are freed by a call to [**MPI\_Request\_free**](mpi-request-free-function.md) (no call to **MPI\_{Wait|Test}{any|some|all}** will occur for such a request). In this case, the callback function will be called either in the MPI call [**MPI\_Request\_free**](mpi-request-free-function.md), or in the MPI call [**MPI\_Grequest\_complete**](mpi-grequest-complete-function.md), whichever happens last, i.e., in this case the actual freeing code is executed as soon as both calls [**MPI\_Request\_free**](mpi-request-free-function.md) and [**MPI\_Grequest\_complete**](mpi-grequest-complete-function.md) have occurred. The request is not deallocated until after *free\_fn* completes. Note that *free\_fn* will be invoked only once per request by a correct program.

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

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Testany**](mpi-testany-function.md)
