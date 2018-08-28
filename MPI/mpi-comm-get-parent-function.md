---
title: MPI_Comm_get_parent function
TOCTitle: MPI_Comm_get_parent function
ms:assetid: cddf7e1a-4fb4-4c76-b4de-4377b94fa72e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473274(v=VS.85)
ms:contentKeyID: 59360820
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_GET_PARENT
- mpif/MPI_Comm_get_parent
- mpi/MPI_COMM_GET_PARENT
dev_langs:
- C++
- C
---

# MPI\_Comm\_get\_parent function

TBD

## Syntax

``` c++
int MPIAPI MPI_Comm_get_parent(
  _Out_ MPI_Comm *parent
);
```

## Parameters

  - *parent* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_COMM_GET_PARENT(PARENT, IERROR)
        INTEGER PARENT, IERROR

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

