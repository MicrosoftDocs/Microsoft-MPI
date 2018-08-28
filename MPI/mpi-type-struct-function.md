---
title: MPI_Type_struct function
TOCTitle: MPI_Type_struct function
ms:assetid: 73fbdd24-782c-41a4-b277-fa3aee6cbb79
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520582(v=VS.85)
ms:contentKeyID: 59361053
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_STRUCT
- mpif/MPI_Type_struct
- mpi/MPI_TYPE_STRUCT
dev_langs:
- C++
- C
---

# MPI\_Type\_struct function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_create\_struct**](mpi-type-create-struct-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Type_struct(
   int        count,
   _In_count_ newtype
);
```

## Parameters

  - *count*  
    TBD

  - *newtype*  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_STRUCT(COUNT, ARRAY_OF_BLOCKLENGTHS,
                ARRAY_OF_DISPLACEMENTS, ARRAY_OF_TYPES, NEWTYPE, IERROR)
        INTEGER COUNT, ARRAY_OF_BLOCKLENGTHS(*), ARRAY_OF_TYPES(*), NEWTYPE,
        IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ARRAY_OF_DISPLACEMENTS(*)

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

[**MPI\_Type\_create\_struct**](mpi-type-create-struct-function.md)

