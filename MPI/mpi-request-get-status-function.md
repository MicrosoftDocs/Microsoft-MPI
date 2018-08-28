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
---

# MPI\_Request\_get\_status function

TBD

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
    TBD

  - *flag* \[out\]  
    TBD

  - *status* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_REQUEST_GET_STATUS( REQUEST, FLAG, STATUS, IERROR)
        INTEGER REQUEST, STATUS(MPI_STATUS_SIZE), IERROR
        LOGICAL FLAG

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

