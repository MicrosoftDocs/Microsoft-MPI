---
title: MPI_Startall function
TOCTitle: MPI_Startall function
ms:assetid: ffd68b75-c72e-4d48-aad8-103154f6bddc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473474(v=VS.85)
ms:contentKeyID: 59361009
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SSEND_INIT
- mpi/MPI_SSEND_INIT
- mpi/MPI_Startall
- MPI_Startall
- mpif/MPI_SSEND_INIT
- mpif/MPI_Startall
dev_langs:
- C++
- C
description: Learn about the MPI_Startall function on Microsoft's official site. Understand its syntax, parameters, return values, and usage considerations.
---

# MPI\_Startall function

Starts a collection of persistent requests.

## Syntax

``` c++
int MPIAPI MPI_Startall(
   int                              count,
   _Inout_count_(count) MPI_Request *array_of_requests
);
```

## Parameters

  - *count*  
    Size of the request array.

  - *array\_of\_requests*  
    Array of requests.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_STARTALL(COUNT, ARRAY_OF_REQUESTS, IERROR)
        INTEGER COUNT, ARRAY_OF_REQUESTS(*), IERROR
```

## Remarks

Unlike [**MPI\_Waitall**](mpi-waitall-function.md), [**MPI\_Startall**](mpi-startall-function.md) does not provide a mechanism for returning multiple errors nor pinpointing the request(s) involved. Futhermore, the behavior of [**MPI\_Startall**](mpi-startall-function.md) after an error occurs is not defined by the MPI standard.  If well-defined error reporting and behavior are required, multiple calls to [**MPI\_Start**](mpi-start-function.md) should be used instead.

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

