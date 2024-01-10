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
    Extra state.

  - *status* \[out\]  
    MPI status object.

## Return value

All callback functions return an error code. The code is passed back and dealt with as appropriate for the error code by the MPI function that invoked the callback function. For example, if error codes are returned then the error code returned by the callback function will be returned by the MPI function that invoked the callback function. In the case of an **MPI\_{Wait|Test}any** call that invokes both *query\_fn* and *free\_fn*, the MPI call will return the error code returned by the last callback, namely *free\_fn*. If one or more of the requests in a call to **MPI\_{Wait|Test}{some|all}** failed, then the MPI call will return **MPI\_ERR\_IN\_STATUS**. In such a case, if the MPI call was passed an array of statuses, then MPI will return in each of the statuses that correspond to a completed generalized request the error code returned by the corresponding invocation of its *free\_fn* callback function. However, if the MPI function was passed **MPI\_STATUSES\_IGNORE**, then the individual error codes returned by each callback functions will be lost.

## Fortran

``` FORTRAN
    SUBROUTINE GREQUEST_QUERY_FUNCTION(EXTRA_STATE, STATUS, IERROR)
        INTEGER STATUS(MPI_STATUS_SIZE), IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
```

## Remarks

The *query\_fn* function computes the status that should be returned for the generalized request. The status also includes information about successful/unsuccessful cancellation of the request (result to be returned by [**MPI\_Test\_cancelled**](mpi-test-cancelled-function.md)).

The *query\_fn* callback is invoked by the **MPI\_{Wait|Test}{any|some|all}** call that completed the generalized request associated with this callback. The callback function is also invoked by calls to [**MPI\_Request\_get\_status**](mpi-request-get-status-function.md), if the request is complete when the call occurs. In both cases, the callback is passed a reference to the corresponding status variable passed by the user to the MPI call; the status set by the callback function is returned by the MPI call. If the user provided **MPI\_STATUS\_IGNORE** or **MPI\_STATUSES\_IGNORE** to the MPI function that causes *query\_fn* to be called, then MPI will pass a valid status object to *query\_fn*, and this status will be ignored upon return of the callback function. Note that *query\_fn* is invoked only after [**MPI\_Grequest\_complete**](mpi-grequest-complete-function.md) is called on the request; it may be invoked several times for the same generalized request, e.g., if the user calls [**MPI\_Request\_get\_status**](mpi-request-get-status-function.md) several times for this request. Note also that a call to **MPI\_{Wait|Test}{some|all}** may cause multiple invocations of *query\_fn* callback functions, one for each generalized request that is completed by the MPI call. The order of these invocations is not specified by MPI.

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

