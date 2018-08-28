---
title: MPI_Comm_set_errhandler function
TOCTitle: MPI_Comm_set_errhandler function
ms:assetid: 6e529f19-8012-4dd6-aaa0-1846088bf051
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473281(v=VS.85)
ms:contentKeyID: 59360827
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SET_ERRHANDLER
- mpif/MPI_Comm_set_errhandler
- mpi/MPI_COMM_SET_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Comm\_set\_errhandler function

TBD

## Syntax

``` c++
int MPIAPI MPI_Comm_set_errhandler(
   MPI_Comm       comm,
   MPI_Errhandler errhandler
);
```

## Parameters

  - *comm*  
    TBD

  - *errhandler*  
    TBD

## Return value

TBD

## Fortran

    MPI_COMM_SET_ERRHANDLER(COMM, ERRHANDLER, IERROR)
        INTEGER COMM, ERRHANDLER, IERROR

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

[MPI Management Functions](mpi-management-functions.md)

