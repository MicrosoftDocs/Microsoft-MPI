---
title: MPI_Type_get_attr function
TOCTitle: MPI_Type_get_attr function
ms:assetid: 768195eb-e79e-4041-bb03-387d74f1d468
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520568(v=VS.85)
ms:contentKeyID: 59361039
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_ATTR
- mpif/MPI_Type_get_attr
- mpi/MPI_TYPE_GET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_attr function

Retrieves attribute value by key.

## Syntax

``` c++
int MPIAPI MPI_Type_get_attr(
        MPI_Datatype type,
        int          type_keyval,
  _Out_ void         *attribute_val,
  _Out_ int          *flag
);
```

## Parameters

  - *type*  
    Datatype to which the attribute is attached.

  - *type\_keyval*  
    Key value.

  - *attribute\_val* \[out\]  
    Attribute value, unless *flag* is false.

  - *flag* \[out\]  
    False if no attribute is associated with the key.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_GET_ATTR(DATATYPE, TYPE_KEYVAL, ATTRIBUTE_VAL, FLAG, IERROR)
        INTEGER DATATYPE, TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL
```

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

