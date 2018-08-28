---
title: MPI_Pack_external_size function
TOCTitle: MPI_Pack_external_size function
ms:assetid: 03fb67d7-1610-4a99-ad87-4b8bdaf73b7c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473442(v=VS.85)
ms:contentKeyID: 59360978
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PACK_EXTERNAL_SIZE
- mpif/MPI_Pack_external_size
- mpi/MPI_PACK_EXTERNAL_SIZE
dev_langs:
- C++
- C
---

# MPI\_Pack\_external\_size function

TBD

## Syntax

``` c++
int MPIAPI MPI_Pack_external_size(
        _In_z_ char  *datarep,
        int          incount,
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *size
);
```

## Parameters

  - *datarep*  
    TBD

  - *incount*  
    TBD

  - *datatype*  
    TBD

  - *size* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_PACK_EXTERNAL_SIZE(DATAREP, INCOUNT, DATATYPE, SIZE, IERROR)
        INTEGER INCOUNT, DATATYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
        CHARACTER*(*) DATAREP

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

