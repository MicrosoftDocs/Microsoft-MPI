---
title: MPI_Type_set_attr function
TOCTitle: MPI_Type_set_attr function
ms:assetid: 209ea154-8c25-46ec-8bf9-eca8e5e26b42
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520579(v=VS.85)
ms:contentKeyID: 59361050
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_SET_ATTR
- mpif/MPI_Type_set_attr
- mpi/MPI_TYPE_SET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Type\_set\_attr function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_set_attr(
       MPI_Datatype type,
       int          type_keyval,
  _In_ void         *attribute_val
);
```

## Parameters

  - *type*  
    TBD

  - *type\_keyval*  
    TBD

  - *attribute\_val* \[in\]  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_SET_ATTR(DATATYPE, TYPE_KEYVAL, ATTRIBUTE_VAL, IERROR)
        INTEGER DATATYPE, TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL

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

[MPI Caching Functions](mpi-caching-functions.md)

