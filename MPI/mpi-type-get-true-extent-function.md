---
title: MPI_Type_get_true_extent function
TOCTitle: MPI_Type_get_true_extent function
ms:assetid: a55f4c95-e51f-48ac-a965-ccd403c9bd71
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520573(v=VS.85)
ms:contentKeyID: 59361044
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_TRUE_EXTENT
- mpif/MPI_Type_get_true_extent
- mpi/MPI_TYPE_GET_TRUE_EXTENT
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_true\_extent function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_get_true_extent(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *true_lb,
  _Out_ MPI_Aint     *true_extent
);
```

## Parameters

  - *datatype*  
    TBD

  - *true\_lb* \[out\]  
    TBD

  - *true\_extent* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_GET_TRUE_EXTENT(DATATYPE, TRUE_LB, TRUE_EXTENT, IERROR)
        INTEGER DATATYPE, IERROR
        INTEGER(KIND = MPI_ADDRESS_KIND) TRUE_LB, TRUE_EXTENT

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

