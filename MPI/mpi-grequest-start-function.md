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
description: Learn about the MPI_Grequest_start function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements for HPC Packs.
---

# MPI\_Grequest\_start function

Creates and returns a user-defined request.

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
    Callback function invoked when request status is queried.

  - *free\_fn* \[in\]  
    Callback function invoked when request is freed.

  - *cancel\_fn* \[in\]  
    Callback function invoked when request is cancelled.

  - *extra\_state* \[in, optional\]  
    Extra state passed to the above functions.

  - *request* \[out\]  
    Generalized request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GREQUEST_START(QUERY_FN, FREE_FN, CANCEL_FN, EXTRA_STATE, REQUEST, IERROR)
        INTEGER REQUEST, IERROR
        EXTERNAL QUERY_FN, FREE_FN, CANCEL_FN
        INTEGER (KIND=MPI_ADDRESS_KIND) EXTRA_STATE
```

## Remarks

The return values from the callback functions must be a valid MPI error code or class.  This value may either be the return value from any MPI routine (with one exception noted below) or any of the MPI error classes. For portable programs, **MPI\_ERR\_OTHER** may be used; to provide more specific information, create a new MPI error class or code with [**MPI\_Add\_error\_class**](mpi-add-error-class-function.md) or [**MPI\_Add\_error\_code**](mpi-add-error-code-function.md) and return that value.

The MPI standard is not clear on the return values from the callback routines. However, there are notes in the standard that imply that these are MPI error codes.  For example, pages 169 line 46 through page 170, line 1 require that the *free_fn* return an MPI error code that may be used in the MPI completion functions when they return **MPI\_ERR\_IN\_STATUS**.

The one special case is the error value returned by [**MPI\_Comm\_dup**](mpi-comm-dup-function.md) when the attribute callback routine returns a failure.  The MPI standard is not clear on what values may be used to indicate an error return.  Further, the Intel MPI test suite made use of non-zero values to indicate failure, and expected these values to be returned by the [**MPI\_Comm\_dup**](mpi-comm-dup-function.md) when the attribute routines encountered an error.  Such error values may not be valid MPI error codes or classes.  Because of this, it is the user's responsibility to either use valid MPI error codes in return from the attribute callbacks, if those error codes are to be returned by a generalized request callback, or to detect and convert those error codes to valid MPI error codes (recall that MPI error classes are valid error codes).

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

[MPI External Functions](mpi-external-functions.md)

[*MPI\_Grequest\_query\_function*](mpi-grequest-query-function-callback-function.md)

[*MPI\_Grequest\_free\_function*](mpi-grequest-free-function-callback-function.md)

[*MPI\_Grequest\_cancel\_function*](mpi-grequest-cancel-function-callback-function.md)

