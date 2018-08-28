---
title: MPI_Type_create_f90_complex function
TOCTitle: MPI_Type_create_f90_complex function
ms:assetid: a88fa355-14bb-4e57-9e5f-156552b747e6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473488(v=VS.85)
ms:contentKeyID: 59361023
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_F90_COMPLEX
- mpif/MPI_Type_create_f90_complex
- mpi/MPI_TYPE_CREATE_F90_COMPLEX
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_f90\_complex function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_create_f90_complex(
        int          p,
        int          r,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *p*  
    TBD

  - *r*  
    TBD

  - *newtype* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_CREATE_F90_COMPLEX(P, R, NEWTYPE, IERROR)
        INTEGER P, R, NEWTYPE, IERROR

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

