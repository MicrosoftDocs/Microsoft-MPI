---
title: MPI_Type_commit function
TOCTitle: MPI_Type_commit function
ms:assetid: 7530b8e4-b739-486c-b866-4f3672054934
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473484(v=VS.85)
ms:contentKeyID: 59361019
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_COMMIT
- mpif/MPI_Type_commit
- mpi/MPI_TYPE_COMMIT
dev_langs:
- C++
- C
---

# MPI\_Type\_commit function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_commit(
  _In_ MPI_Datatype *datatype
);
```

## Parameters

  - *datatype* \[in\]  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_COMMIT(DATATYPE, IERROR)
        INTEGER DATATYPE, IERROR

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

[MPI Datatype Functions](mpi-datatype-functions.md)

