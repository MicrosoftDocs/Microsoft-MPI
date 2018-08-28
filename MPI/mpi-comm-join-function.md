---
title: MPI_Comm_join function
TOCTitle: MPI_Comm_join function
ms:assetid: 3c07220f-07c9-4fa4-ba9f-52160c29100e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473276(v=VS.85)
ms:contentKeyID: 59360822
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_JOIN
- mpif/MPI_Comm_join
- mpi/MPI_COMM_JOIN
dev_langs:
- C++
- C
---

# MPI\_Comm\_join function

TBD

## Syntax

``` c++
int MPIAPI MPI_Comm_join(
        int      fd,
  _Out_ MPI_Comm *intercomm
);
```

## Parameters

  - *fd*  
    TBD

  - *intercomm* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_COMM_JOIN(FD, INTERCOMM, IERROR)
        INTEGER FD, INTERCOMM, IERROR

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

[MPI Process Management Functions](mpi-process-management-functions.md)

