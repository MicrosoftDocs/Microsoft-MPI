---
title: MPI_Get_processor_name function
TOCTitle: MPI_Get_processor_name function
ms:assetid: cdbe3718-c1f5-4c6c-a34a-2263c76ee30d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473382(v=VS.85)
ms:contentKeyID: 59360918
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_PROCESSOR_NAME
- mpif/MPI_Get_processor_name
- mpi/MPI_GET_PROCESSOR_NAME
dev_langs:
- C++
- C
---

# MPI\_Get\_processor\_name function

TBD

## Syntax

``` c++
int MPIAPI MPI_Get_processor_name(
        _Out_z_cap_post_count_(MPI_MAX_PROCESSOR_NAME,*resultlen) char *name,
  _Out_ int                                                            *resultlen
);
```

## Parameters

  - *name*  
    TBD

  - *resultlen* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_GET_PROCESSOR_NAME( NAME, RESULTLEN, IERROR)
        CHARACTER*(*) NAME
        INTEGER RESULTLEN,IERROR

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

