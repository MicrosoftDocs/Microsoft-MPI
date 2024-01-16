---
title: MPI_Request_get_status function
TOCTitle: MPI_Request_get_status function
ms:assetid: 31c598c3-0b5e-4509-9357-93c6d4f20bdd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473461(v=VS.85)
ms:contentKeyID: 59360996
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REQUEST_GET_STATUS
- mpif/MPI_Request_get_status
- mpi/MPI_REQUEST_GET_STATUS
dev_langs:
- C++
- C
description: Learn about MPI_Request_get_status function on Microsoft's site. Understand its syntax, parameters, return value, and how it differs from MPI_Test.
---

# MPI\_Request\_get\_status function

Nondestructive test for the completion of a request.

## Syntax

``` c++
int MPIAPI MPI_Request_get_status(
        MPI_Request request,
  _Out_ int         *flag,
  _Out_ MPI_Status  *status
);
```

## Parameters

  - *request*  
    Communication request.

  - *flag* \[out\]  
    True if operation has completed.

  - *status* \[out\]  
    Status object, or **MPI\_STATUS\_IGNORE**.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_REQUEST_GET_STATUS( REQUEST, FLAG, STATUS, IERROR)
        INTEGER REQUEST, STATUS(MPI_STATUS_SIZE), IERROR
        LOGICAL FLAG
```

## Remarks

Unlike [**MPI\_Test**](mpi-test-function.md), [**MPI\_Request\_get\_status**](mpi-request-get-status-function.md) does not deallocate or deactivate the request.  A call to one of the test/wait routines or [**MPI\_Request\_free**](mpi-request-free-function.md) should be made to release the request object.

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

