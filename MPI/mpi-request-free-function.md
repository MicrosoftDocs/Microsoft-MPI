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

TBD

## Syntax

``` c++
int MPIAPI MPI_Request_free(
   _Inout_ MPI_Request *request
);
```

## Parameters

  - *request*  
    TBD

## Return value

TBD

## Fortran

    MPI_REQUEST_FREE(REQUEST, IERROR)
        INTEGER REQUEST, IERROR

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

