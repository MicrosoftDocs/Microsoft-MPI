---
title: MPI_Cancel function
TOCTitle: MPI_Cancel function
ms:assetid: c0393047-75f3-4ae1-bd02-94be1d8798f1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473243(v=VS.85)
ms:contentKeyID: 59360789
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CANCEL
- mpif/MPI_Cancel
- mpi/MPI_CANCEL
dev_langs:
- C++
- C
description: Explore MPI_Cancel function on Microsoft's learning platform. Understand its syntax, parameters, return values, and its use in multi-buffering schemes.
---

# MPI\_Cancel function

Cancels a communication request.

## Syntax

``` c++
int MPIAPI MPI_Cancel(
  _In_ MPI_Request *request
);
```

## Parameters

  - *request* \[in\]  
    Communication request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CANCEL(REQUEST, IERROR)
        INTEGER REQUEST, IERROR
```

## Remarks

The primary expected use of **MPI\_Cancel** is in multi-buffering schemes, where speculative **MPI\_Irecv**s are made.  When the computation completes, some of these receive requests may remain; using **MPI\_Cancel** allows the user to cancel these unsatisfied requests.

Cancelling a send operation is much more difficult, in large part because the send will usually be at least partially complete (the information on the tag, size, and source are usually sent immediately to the destination).
Users are advised that cancelling a send, while a local operation (as defined by the MPI standard), is likely to be expensive (usually generating one or more internal messages).

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

