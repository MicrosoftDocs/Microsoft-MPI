---
title: MPI_Free_mem function
TOCTitle: MPI_Free_mem function
ms:assetid: a951f728-1745-4298-804f-f0374d7372bb
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473374(v=VS.85)
ms:contentKeyID: 59360910
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FREE_MEM
- mpif/MPI_Free_mem
- mpi/MPI_FREE_MEM
dev_langs:
- C++
- C
---

# MPI\_Free\_mem function

TBD

## Syntax

``` c++
int MPIAPI MPI_Free_mem(
  _In_ void *base
);
```

## Parameters

  - *base* \[in\]  
    TBD

## Return value

TBD

## Fortran

    MPI_FREE_MEM(BASE, IERROR)
        <type> BASE(*)
        INTEGER IERROR

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

