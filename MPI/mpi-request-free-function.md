---
title: MPI_Request_free function
TOCTitle: MPI_Request_free function
ms:assetid: f89b1d2f-52c1-48e4-8e59-ba7c3f361706
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473460(v=VS.85)
ms:contentKeyID: 59360995
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REQUEST_FREE
- mpif/MPI_Request_free
- mpi/MPI_REQUEST_FREE
dev_langs:
- C++
- C
---

# MPI\_Request\_free function

Frees a communication request object.

## Syntax

``` c++
int MPIAPI MPI_Request_free(
   _Inout_ MPI_Request *request
);
```

## Parameters

  - *request*  
    Communication request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_REQUEST_FREE(REQUEST, IERROR)
        INTEGER REQUEST, IERROR
```

## Remarks

This routine is normally used to free inactive persistent requests created with either [**MPI\_Recv\_init**](mpi-recv-init-function.md) or [**MPI\_Send\_init**](mpi-send-init-function.md) and friends.  It is also permissible to free an active request.  However, once freed, the request can no longer be used in a wait or test routine (e.g., [**MPI\_Wait**](mpi-wait-function.md)) to determine completion.

This routine may also be used to free a non-persistent requests such as those created with [**MPI\_Irecv**](mpi-irecv-function.md) or [**MPI\_Isend**](mpi-isend-function.md) and friends.  Like active persistent requests, once freed, the request can no longer be used with test/wait routines to determine completion.

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

